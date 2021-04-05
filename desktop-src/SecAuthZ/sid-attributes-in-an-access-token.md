---
description: Jede Benutzer-und Gruppen Sicherheits-ID (SID) in einem Zugriffs Token verfügt über eine Reihe von Attributen, mit denen gesteuert wird, wie das System die SID in einer Zugriffs Überprüfung verwendet. In der folgenden Tabelle werden die Attribute aufgelistet, die die Zugriffs Überprüfung steuern.
ms.assetid: c902f876-f05e-4b0c-ab65-a0c6cebca933
title: SID-Attribute in einem Zugriffs Token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a93e180c8c6ffe03a26591d5b9f722c2266356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752744"
---
# <a name="sid-attributes-in-an-access-token"></a>SID-Attribute in einem Zugriffs Token

Jede Benutzer-und Gruppen [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) in einem [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) verfügt über eine Reihe von Attributen, mit denen gesteuert wird, wie das System die SID in einer Zugriffs Überprüfung verwendet. In der folgenden Tabelle werden die Attribute aufgelistet, die die Zugriffs Überprüfung steuern.



| Attribut                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_aktivierte SE-Gruppe \_              | Eine SID mit diesem Attribut ist für Zugriffs Überprüfungen aktiviert. Wenn das System eine Zugriffs Überprüfung durchführt, prüft es auf Zugriffs zugelassene [*Zugriffs Steuerungs Einträge (Access Control Entries*](/windows/desktop/SecGloss/a-gly) , ACEs), die auf eine der aktivierten SIDs im Zugriffs Token angewendet werden. Eine SID ohne dieses Attribut wird während einer Zugriffs Überprüfung ignoriert, es sei denn, die SE- \_ Gruppe \_ \_ \_ wird nur für das deny- \_ Attribut festgelegt.<br/> |
| Verwendung der SE- \_ Gruppe \_ \_ \_ nur für deny \_ | Eine SID mit diesem Attribut ist eine nur-verweigern-sid. Wenn das System eine Zugriffs Überprüfung durchführt, prüft es auf Zugriffs Verweigerungs-ACEs, die für die SID gelten, aber es ignoriert Zugriffs zulässige ACEs für die SID. Wenn dieses Attribut festgelegt ist, \_ wird das \_ Attribut für die SE-Gruppen Aktivierung nicht festgelegt, und die SID kann nicht erneut aktiviert werden.<br/>                                                                                                                                                          |



 

\_Verwenden Sie die Funktion "Funktion", um das Attribut der Gruppe "Gruppen-SID" zu aktivieren oder zu löschen \_ . [](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) Es ist nicht möglich, eine Gruppen-SID mit dem obligatorischen Attribut der SE-Gruppe zu deaktivieren \_ \_ . Sie können die Benutzer-SID eines Zugriffs Tokens nicht mithilfe von " **resoltokengroups** " deaktivieren.

Um zu ermitteln, ob eine SID in einem Token aktiviert ist, d. h., ob Sie über das Attribut "SE Group" verfügt, müssen Sie \_ \_ die [**checktokenmembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership) -Funktion aufzurufen.

Wenn Sie die Gruppe "SE" \_ \_ für " \_ \_ nur ablehnen" einer SID festlegen möchten \_ , schließen Sie die SID in die Liste der nur Verweigerungs-SIDs ein, die Sie beim Aufrufen der Funktion "| [**aterestrictedtoken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) " angeben. Mit " **anaterestrictedtoken** " kann die Gruppe "SE" \_ für " \_ \_ \_ nur ablehnen" \_ auf eine beliebige sid angewendet werden, einschließlich der Benutzer-SID und der Gruppen-SIDs, die das \_ obligatorische Attribut der SE-Gruppe \_ Allerdings können Sie das Attribut "Deny-only" nicht aus einer SID entfernen, und Sie können "" "" "" " [**" mit "**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) " "" "die \_ Gruppen aktivierten Attribute" SE "nicht für \_ eine SID festlegen

Um die Attribute einer SID abzurufen, wenden Sie die [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) -Funktion mit dem tokenGroups-Wert an. Die-Funktion gibt ein Array aus [**sid \_ -und \_ Attribute-**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) Strukturen zurück, die die Gruppen-SIDs und deren Attribute identifizieren.

 

