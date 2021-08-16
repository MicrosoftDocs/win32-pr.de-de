---
description: Wenn ein Windows-Objekt nicht über eine DACL (Discretionary Access Control List) verfügt, ermöglicht das System jedem Vollzugriff darauf.
ms.assetid: be9633fb-14ef-42d2-9269-84287b35b653
title: DACLs und ACEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07bf87c2bd5f64b7178eca9d9fedd695a8b618430bf505f74be297780e48f774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782179"
---
# <a name="dacls-and-aces"></a>DACLs und ACEs

Wenn ein Windows-Objekt nicht über eine DACL [*(Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) verfügt, ermöglicht das System jedem Vollzugriff darauf. Wenn ein Objekt über eine DACL verfügt, lässt das System [](/windows/desktop/SecGloss/a-gly) nur den Zugriff zu, der explizit von den Zugriffssteuerungseinträgen (ACEs) in der DACL zugelassen wird. Wenn die DACL keine ACEs enthält, lässt das System keinen Zugriff für personen zu. Wenn eine DACL über ACEs verfügt, die den Zugriff auf eine begrenzte Gruppe von Benutzern oder Gruppen zulassen, verweigert das System implizit den Zugriff für alle Vertrauenshänder, die nicht in den ACEs enthalten sind.

In den meisten Fällen können Sie den Zugriff auf ein Objekt mithilfe von zugriffs zulässigen ACEs steuern. Sie müssen den Zugriff auf ein Objekt nicht explizit verweigern. Eine Ausnahme ist, wenn ein ACE den Zugriff auf eine Gruppe zulässt und Sie einem Mitglied der Gruppe den Zugriff verweigern möchten. Platzieren Sie dazu einen zugriffsgeementierten ACE für den Benutzer in der DACL vor dem für den Zugriff zulässigen ACE für die Gruppe. Beachten Sie, [dass die Reihenfolge der ACEs](order-of-aces-in-a-dacl.md) wichtig ist, da das System die ACEs nacheinander liest, bis der Zugriff gewährt oder verweigert wird. Der ZUGRIFFS verweigerte ACE des Benutzers muss zuerst angezeigt werden. Andernfalls gewährt das System dem eingeschränkten Benutzer Zugriff, wenn es den zugriffsberechtigungsbeschränkten ACE der Gruppe liest.

Die folgende Abbildung zeigt eine DACL, die einem Benutzer den Zugriff verweigert und zwei Gruppen Zugriff gewährt. Die Mitglieder von Gruppe A erhalten Lese-, Schreib- und Ausführungszugriffsrechte, indem sie die für Gruppe A zulässigen Rechte und die für alle zulässigen Rechte akkumulieren. Eine Ausnahme bildet Andrew, dem der Zugriff durch den ace verweigert wird, obwohl er Mitglied der Gruppe "Jeder" ist.

![Dacl, die unterschiedliche Zugriffsrechte basierend auf der Gruppenmitgliedschaft gewährt](images/accctrl1.png)

 

 
