---
title: Einstiegspunkte für Autorisierungs-Plug-ins
description: Einstiegspunkte für Autorisierungs-Plug-ins
ms.assetid: 6cbfa79a-b57b-44b8-a421-d5e79c1b3757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee0db76457860106e51bd6c29cead3d0f8227d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342369"
---
# <a name="authorization-plug-in-entry-points"></a>Einstiegspunkte für Autorisierungs-Plug-ins

Autorisierungs-Plug-ins werden nur für einen Internetinformationsdienste (IIS)-Host Prozess konfiguriert. Pro virtuellem Verzeichnis kann nur ein Autorisierungs-Plug-in konfiguriert werden.

Alle Autorisierungs-Plug-Ins müssen die folgenden Einstiegspunkte unterstützen:

-   [**Wsmanpluginstartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)
-   [**Wsmanpluginshutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)
-   [**Wsmanpluginauthzuser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)
-   [**Wsmanpluginauthzoperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)

Der folgende Einstiegspunkt ist optional:

-   [**Wsmanpluginauthzqueryquota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)

In der folgenden Tabelle finden Sie eine Übersicht über die Einstiegspunkte des Autorisierungs-Plug-ins in der Windows-Remoteverwaltung-Plug-in-API (WinRM).



| Funktion                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSMAN- \_ Plugin- \_ Autorisierungs \_ Vorgang**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)              | Wird aufgerufen, um einen bestimmten Vorgang zu autorisieren. <br/> Der Name des dll-Einstiegs Punkts für diese Methode muss " [**wsmanpluginauthzoperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)" lauten.<br/>                                                                                                                                                                                                       |
| [**WSMAN-Plug-in, \_ \_ Autorisierungs \_ \_ Kontingent**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)           | Wird aufgerufen, nachdem eine Verbindung autorisiert wurde, Kontingent Informationen für den Benutzer abzurufen. <br/> Der Name des dll-Einstiegs Punkts für diese Methode muss " [**wsmanpluginauthzqueryquota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)" lauten.<br/>                                                                                                                                                    |
| [**WSMAN-Plug-in, \_ \_ Autorisierungs \_ \_ Kontext**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context) | Wird aufgerufen, um den kontextfrei zugeben, den ein Plug-in entweder von der [**wsmanpluginauthzusercomplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) -Methode oder der [**wsmanpluginauthzoperationcomplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) -Methode meldet. <br/> Der Name des dll-Einstiegs Punkts für diese Methode muss " [**wsmanpluginauthzreleasecontext**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context)" lauten.<br/> |
| [**WSMAN- \_ Plugin- \_ Autorisierung \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)                         | Wird aufgerufen, um zu bestimmen, ob der Benutzer eine Anforderung ausführen darf. <br/> Der Name des Einstiegs Punkts für die Dynamic Link Library (dll) für diese Methode muss " [**wsmanpluginauthzuser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)" lauten.<br/>                                                                                                                                                            |



 

 

