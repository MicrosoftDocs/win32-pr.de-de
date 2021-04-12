---
title: Einstiegspunkte des Vorgangs-Plug-ins
description: Einstiegspunkte des Vorgangs-Plug-ins
ms.assetid: 9a3ddc2b-9fde-4915-b0e8-0a5e79e73c00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0834363c7447bc50269da09d361e630d9bc0615a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473148"
---
# <a name="operations-plug-in-entry-points"></a>Einstiegspunkte des Vorgangs-Plug-ins

Ein Operations-Plug-in muss bestimmte Einstiegspunkte in Abhängigkeit von den Funktionen implementieren, die unterstützt werden sollen.

Ein Plug-in muss beim Windows-Remoteverwaltung-Dienst (WinRM) registriert werden, der die Namen der Plug-in-DLL-Einstiegspunkte enthält. Alle Vorgänge verfügen über vordefinierte DLL-Einstiegspunkte, die verfügbar gemacht werden müssen, wenn dieser Vorgang unterstützt wird.

In der folgenden Tabelle finden Sie eine Übersicht über die Plug-in-Einstiegspunkte für Vorgänge in der WinRM-Plug-in-API.



| Funktion                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSMAN- \_ Plugin- \_ Befehl**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)                                   | Definiert den Befehls Rückruf für ein Plug-in.<br/> Alle WinRM-Plug-ins, die Shellfunktionen unterstützen, müssen diesen Rückruf implementieren.<br/> Der Name des dll-Einstiegs Punkts für diese Methode muss " [**wsmanplugincommand**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)" lauten.<br/> |
| [**WSMAN-Plug-in \_ \_ verbinden**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)                                   | Definiert den Verbindungs Rückruf für ein Plug-in.<br/> Der Name des dll-Einstiegs Punkts für diese Methode muss " [**wsmanpluginconnect**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)" lauten.<br/>                                                                                                |
| [**WSMAN-Plug-in \_ \_ empfangen**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)                                   | Definiert den Empfangs Rückruf für ein Plug-in.<br/> Alle WinRM-Plug-ins, die Shellfunktionen unterstützen, müssen diesen Rückruf implementieren.<br/> Der Name des dll-Einstiegs Punkts für diese Methode muss " [**wsmanpluginreceive**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)" lauten.<br/> |
| [**WSMAN-Plug-in- \_ \_ Freigabe \_ Befehls \_ Kontext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context) | Definiert den Freigabe Befehls Rückruf für das Plug-in.<br/> Der Name des dll-Einstiegs Punkts muss " [**wsmanpluginreleasecommandcontext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context)" lauten.<br/>                                                                        |
| [**WSMAN-Plug-in- \_ \_ Freigabe \_ \_ shellkontext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_shell_context)     | Definiert den releaseshellrückruf für das Plug-in.<br/> Der Name des dll-Einstiegs Punkts muss " [**wsmanpluginreleasecommandcontext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context)" lauten.<br/>                                                                          |
| [**WSMAN-Plug-in \_ \_ senden**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)                                         | Definiert den Sende Rückruf für ein Plug-in.<br/> Alle WinRM-Plug-ins, die Shellfunktionen unterstützen, müssen diesen Rückruf implementieren.<br/> Der Name des dll-Einstiegs Punkts für diese Methode muss " [**wsmanpluginsend**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)" lauten.<br/>          |
| [**WSMAN- \_ Plugin- \_ Shell**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)                                       | Definiert den shellrückruf für ein Plug-in.<br/> Alle WinRM-Plug-ins, die Shellfunktionen unterstützen, müssen diesen Rückruf implementieren.<br/> Der Name des dll-Einstiegs Punkts für diese Methode muss " [**wsmanpluginshell**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)" lauten.<br/>       |
| [**WSMAN-Plug-in \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)                                 | Definiert den Rückruf für das Plug-in.<br/> Alle WinRM-Plug-Ins müssen diese Rückruffunktion implementieren.<br/> Der Name des dll-Einstiegs Punkts für diese Methode muss " [**wsmanpluginshutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)" lauten.<br/>                      |
| [**WSMAN- \_ Plugin- \_ Signal**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)                                     | Definiert den Signal Rückruf für ein Plug-in.<br/> Alle WinRM-Plug-ins, die Shellfunktionen unterstützen, müssen diesen Rückruf implementieren.<br/> Der Name des dll-Einstiegs Punkts für diese Methode muss " [**wsmanpluginsignal**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)" lauten.<br/>    |
| [**WSMAN-Plug-in \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)                                   | Definiert den Start Rückruf für das Plug-in.<br/> Alle WinRM-Plug-Ins müssen diese Rückruffunktion implementieren.<br/> Der Name des dll-Einstiegs Punkts für diese Methode muss " [**wsmanpluginstartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)" lauten.<br/>                         |



 

 

