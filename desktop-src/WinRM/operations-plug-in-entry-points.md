---
title: Einstiegspunkte des Betriebs-Plug-Ins
description: Einstiegspunkte des Betriebs-Plug-Ins
ms.assetid: 9a3ddc2b-9fde-4915-b0e8-0a5e79e73c00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5941746e8e6b952f2f1cd6f21c697398cb4cbb60b024daa557e65151a0a1cfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412770"
---
# <a name="operations-plug-in-entry-points"></a>Einstiegspunkte des Betriebs-Plug-Ins

Ein Betriebs-Plug-In muss abhängig von den Funktionen, die es unterstützen möchte, bestimmte Einstiegspunkte implementieren.

Ein Plug-In muss sich beim Windows-Remoteverwaltungsdienst (WinRM) registrieren, der die Namen der Plug-In-DLL-Einstiegspunkte enthält. Alle Vorgänge verfügen über vordefinierte DLL-Einstiegspunkte, die verfügbar gemacht werden müssen, wenn dieser Vorgang unterstützt wird.

Die folgende Tabelle enthält eine Übersicht über die Einstiegspunkte des Operations-Plug-Ins in der WinRM-Plug-In-API.



| Funktion                                                                                 | Beschreibung                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_WSMAN-PLUG-IN-BEFEHL \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)                                   | Definiert den Befehlsrückruf für ein Plug-In.<br/> Alle WinRM-Plug-Ins, die Shellfunktionen unterstützen, müssen diesen Rückruf implementieren.<br/> Der DLL-Einstiegspunktname für diese Methode muss [**WSManPluginCommand**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)sein.<br/> |
| [**\_WSMAN-PLUG-IN \_ CONNECT**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)                                   | Definiert den Verbindungsrückruf für ein Plug-In.<br/> Der DLL-Einstiegspunktname für diese Methode muss [**WSManPluginConnect**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)sein.<br/>                                                                                                |
| [**EMPFANGEN DES \_ WSMAN-PLUG-INS \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)                                   | Definiert den Empfangsrückruf für ein Plug-In.<br/> Alle WinRM-Plug-Ins, die Shellfunktionen unterstützen, müssen diesen Rückruf implementieren.<br/> Der DLL-Einstiegspunktname für diese Methode muss [**WSManPluginReceive**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)sein.<br/> |
| [**BEFEHLSKONTEXT FÜR RELEASE DES WSMAN-PLUG-INS \_ \_ \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context) | Definiert den Rückruf des Releasebefehls für das Plug-In.<br/> Der Name des DLL-Einstiegspunkts muss [**WSManPluginReleaseCommandContext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context)sein.<br/>                                                                        |
| [**KONTEXT DER \_ \_ \_ RELEASESHELL DES WSMAN-PLUG-INS \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_shell_context)     | Definiert den Releaseshell-Rückruf für das Plug-In.<br/> Der Name des DLL-Einstiegspunkts muss [**WSManPluginReleaseCommandContext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context)sein.<br/>                                                                          |
| [**SENDEN \_ DES WSMAN-PLUG-INS \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)                                         | Definiert den Senderückruf für ein Plug-In.<br/> Alle WinRM-Plug-Ins, die Shellfunktionen unterstützen, müssen diesen Rückruf implementieren.<br/> Der DLL-Einstiegspunktname für diese Methode muss [**WSManPluginSend**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)sein.<br/>          |
| [**\_WSMAN-PLUG-IN-SHELL \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)                                       | Definiert den Shellrückruf für ein Plug-In.<br/> Alle WinRM-Plug-Ins, die Shellfunktionen unterstützen, müssen diesen Rückruf implementieren.<br/> Der DLL-Einstiegspunktname für diese Methode muss [**WSManPluginShell**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)sein.<br/>       |
| [**HERUNTERFAHREN DES \_ WSMAN-PLUG-INS \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)                                 | Definiert den Rückruf zum Herunterfahren für das Plug-In.<br/> Alle WinRM-Plug-Ins müssen diese Rückruffunktion implementieren.<br/> Der DLL-Einstiegspunktname für diese Methode muss [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)sein.<br/>                      |
| [**\_WSMAN-PLUG-IN-SIGNAL \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)                                     | Definiert den Signalrückruf für ein Plug-In.<br/> Alle WinRM-Plug-Ins, die Shellfunktionen unterstützen, müssen diesen Rückruf implementieren.<br/> Der DLL-Einstiegspunktname für diese Methode muss [**WSManPluginSignal**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)sein.<br/>    |
| [**\_WSMAN-PLUG-IN-START \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)                                   | Definiert den Startrückruf für das Plug-In.<br/> Alle WinRM-Plug-Ins müssen diese Rückruffunktion implementieren.<br/> Der DLL-Einstiegspunktname für diese Methode muss [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)sein.<br/>                         |



 

 

