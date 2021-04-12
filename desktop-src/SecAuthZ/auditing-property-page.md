---
description: Der Zugriffs Steuerungs-Editor kann eine Eigenschaften Seite für die Überwachung enthalten, die es dem Benutzer ermöglicht, die Zugriffs Steuerungs Einträge (Access Control Entries, ACEs) in einer System Zugriffs Steuerungs Liste (SACL) von Objekten anzuzeigen und zu bearbeiten. Weitere Informationen zu SACLs finden Sie unter Access Control Listen (ACLs).
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: Eigenschaften Seite "Überwachung"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7fc85691c93994a764199f0b77d52a7a8a71e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216919"
---
# <a name="auditing-property-page"></a>Eigenschaften Seite "Überwachung"

Der Zugriffs Steuerungs-Editor **kann eine Eigenschaften** Seite für die Überwachung enthalten, die es dem Benutzer ermöglicht, die [*Zugriffs Steuerungs Einträge (Access Control Entries*](/windows/desktop/SecGloss/a-gly) , ACEs) in der [*System-Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) eines Objekts anzuzeigen und zu bearbeiten. Weitere Informationen zu SACLs finden Sie unter [Access Control Listen](access-control-lists.md) (ACLs).

**So zeigen Sie die Eigenschaften Seite "Auditing" an**

-   Klicken Sie auf der [Eigenschaften Seite grundlegende Sicherheit](basic-security-property-page.md)auf **erweitert**. Die **Eigenschaften Seite für die Überwachung** befindet sich auf der Eigenschaften Seite " [Erweiterte Sicherheit](advanced-security-property-sheet.md)".

Wenn Sie die Eigenschaften Seite **Auditing** einschließen möchten, legen Sie die Flags für **Si \_ Advanced** und **Si \_ Edit \_** Überwachungen in der [**Si- \_ Objekt \_ Informations**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) Struktur fest, die von Ihrer [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) -Implementierung zurückgegeben wurde.

 

 
