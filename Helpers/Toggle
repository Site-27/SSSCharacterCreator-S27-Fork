using System;
using CommandSystem;
using SSSCharacterCreator.ServerSpecific;

namespace SSSCharacterCreator.Helpers
{
    [CommandHandler(typeof(RemoteAdminCommandHandler))]
    public class ToggleCC : ICommand
    {
        public string Command => "togglecc";
        public string[] Aliases => new[] { "charactercreator", "togglecharactercreator", "cctoggle", "cc" };
        public string Description => "Toggles the character creator (off by default)";

        public bool Execute(ArraySegment<string> arguments, ICommandSender sender, out string response)
        {
            if (CharacterCreator.IsEnabled == true)
            {
                CharacterCreator.IsEnabled = false;
                response = "Character creator has been disabled.";
            }
            else
            {
                CharacterCreator.IsEnabled = true;
                response = "Character creator has been enabled.";
            }

            return true;
        }
    }
}
