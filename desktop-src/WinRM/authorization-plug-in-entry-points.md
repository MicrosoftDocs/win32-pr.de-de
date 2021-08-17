---
title: Einstiegspunkte für Autorisierungs-Plug-Ins
description: Einstiegspunkte für Autorisierungs-Plug-Ins
ms.assetid: 6cbfa79a-b57b-44b8-a421-d5e79c1b3757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16ca861df6b6546920aaf3f778c61117776ff3861556377b280c990c03711fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324078"
---
# <a name="authorization-plug-in-entry-points"></a>Einstiegspunkte für Autorisierungs-Plug-Ins

Autorisierungs-Plug-Ins werden nur für einen Internetinformationsdienste (IIS)-Hostprozess konfiguriert. Pro virtuellem Verzeichnis kann nur ein Autorisierungs-Plug-In konfiguriert werden.

Alle Autorisierungs-Plug-Ins müssen die folgenden Einstiegspunkte unterstützen:

-   [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)
-   [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)
-   [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)
-   [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)

Der folgende Einstiegspunkt ist optional:

-   [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)

Die folgende Tabelle enthält eine Übersicht über die Autorisierungs-Plug-In-Einstiegspunkte in der Windows-Plug-In-API (WinRM).



| Funktion                                                                                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AUTORISIERUNGSVORGANG DES \_ WSMAN-PLUG-INS \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)              | Wird aufgerufen, um einen bestimmten Vorgang zu autorisieren. <br/> Der NAME des DLL-Einstiegspunkts für diese Methode muss [**WSManPluginAuthzOperation sein.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)<br/>                                                                                                                                                                                                       |
| [**\_WSMAN-PLUG-IN: \_ \_ AUTORISIEREN DES \_ ABFRAGEKONTINGENTS**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)           | Wird aufgerufen, nachdem eine Verbindung autorisiert wurde, Kontingentinformationen für den Benutzer abzurufen. <br/> Der NAME des DLL-Einstiegspunkts für diese Methode muss [**WSManPluginAuthzQueryQuota sein.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)<br/>                                                                                                                                                    |
| [**\_WSMAN-PLUG-IN: \_ \_ AUTORISIEREN DES \_ RELEASEKONTEXTS**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context) | Wird aufgerufen, um den Kontext frei zu geben, den ein Plug-In entweder über die [**Methoden WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) oder [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) meldet. <br/> Der NAME des DLL-Einstiegspunkts für diese Methode muss [**WSManPluginAuthzReleaseContext sein.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context)<br/> |
| [**\_WSMAN-PLUG-IN: \_ AUTORISIEREN DES \_ BENUTZERS**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)                         | Wird aufgerufen, um zu bestimmen, ob der Benutzer eine Anforderung durchführen darf. <br/> Der Name des DLL-Einstiegspunkts (Dynamic Link Library) für diese Methode muss [**WSManPluginAuthzUser sein.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)<br/>                                                                                                                                                            |



 

 

