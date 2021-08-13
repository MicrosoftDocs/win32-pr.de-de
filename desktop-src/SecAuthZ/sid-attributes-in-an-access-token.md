---
description: Jeder Benutzer und jede Gruppensicherheits-ID (SID) in einem Zugriffstoken verfügt über einen Satz von Attributen, die steuern, wie das System die SID in einer Zugriffsüberprüfung verwendet. In der folgenden Tabelle sind die Attribute aufgeführt, die die Zugriffsüberprüfung steuern.
ms.assetid: c902f876-f05e-4b0c-ab65-a0c6cebca933
title: SID-Attribute in einem Zugriffstoken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe504e190e6d6e884b8068eb23983b2bc506c7c8447a8db77fd3ddb9cdfb917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413420"
---
# <a name="sid-attributes-in-an-access-token"></a>SID-Attribute in einem Zugriffstoken

Jeder Benutzer und jede [*Gruppensicherheits-ID*](/windows/desktop/SecGloss/s-gly) (SID) in einem Zugriffstoken verfügt über einen Satz von Attributen, die steuern, wie das System die SID in einer Zugriffsüberprüfung verwendet. [](/windows/desktop/SecGloss/a-gly) In der folgenden Tabelle sind die Attribute aufgeführt, die die Zugriffsüberprüfung steuern.



| attribute                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_SE GROUP \_ ENABLED              | Eine SID mit diesem Attribut ist für Zugriffsüberprüfungen aktiviert. Wenn das System eine Zugriffsüberprüfung durchführt, überprüft es, ob Zugriffs- und Zugriffssteuerungseinträge (Access-Allowed, Access-Denied Access [*Control Entries,*](/windows/desktop/SecGloss/a-gly) ACEs) für eine der aktivierten SIDs im Zugriffstoken gelten. Eine SID ohne dieses Attribut wird während einer Zugriffsüberprüfung ignoriert, es sei denn, das SE \_ GROUP \_ USE FOR \_ \_ DENY \_ ONLY-Attribut ist festgelegt.<br/> |
| \_SE GRUPPENNUTZUNG \_ \_ NUR FÜR \_ VERWEIGERN \_ | Eine SID mit diesem Attribut ist eine SID, die nur zum Verweigern verwendet wird. Wenn das System eine Zugriffsüberprüfung durchführt, sucht es nach Zugriffs verweigerten ACEs, die für die SID gelten. Zugriffsberechtigungen für die SID werden jedoch ignoriert. Wenn dieses Attribut festgelegt ist, wird SE GROUP ENABLED-Attribut nicht festgelegt, und \_ die SID kann nicht erneut aktiviert \_ werden.<br/>                                                                                                                                                          |



 

Verwenden Sie die Funktion \_ \_ [**AdjustTokenGroups,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) um SE GROUP ENABLED-Attribut einer Gruppen-SID fest- oder zu löschen. Sie können keine Gruppen-SID deaktivieren, die über das SE \_ GROUP \_ MANDATORY-Attribut verfügt. Sie können **AdjustTokenGroups nicht verwenden,** um die Benutzer-SID eines Zugriffstokens zu deaktivieren.

Rufen Sie die \_ \_ [**CheckTokenMembership-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership) auf, um zu bestimmen, ob eine SID in einem Token aktiviert ist, d. SE GROUP ENABLED-Attribut.

Um das SE GROUP USE FOR DENY ONLY-Attribut einer SID festzulegen, schließen Sie die SID in die Liste der SIDs ein, die nur zum Verweigern verwendet werden, die Sie beim Aufrufen der \_ \_ \_ \_ \_ [**CreateRestrictedToken-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) angeben. **CreateRestrictedToken** kann das SE GROUP USE FOR DENY ONLY-Attribut auf eine beliebige SID anwenden, einschließlich der Benutzer-SID und \_ der \_ \_ Gruppen-SIDs, die über das SE \_ \_ GROUP MANDATORY-Attribut \_ \_ verfügen. Sie können jedoch weder das Attribut "Nur verweigern" aus einer SID entfernen noch [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) verwenden, um das SE GROUP ENABLED-Attribut für eine \_ \_ NUR-SID für deny-Zugriff festlegen.

Um die Attribute einer SID abzurufen, rufen Sie die [**GetTokenInformation-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) mit dem TokenGroups-Wert auf. Die Funktion gibt ein Array von [**\_ SID- und \_ ATTRIBUTES-Strukturen**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) zurück, die die Gruppen-SIDs und ihre Attribute identifizieren.

 

