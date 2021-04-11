---
description: Wenn ein Windows-Objekt nicht über eine freigegebene Zugriffs Steuerungs Liste (DACL) verfügt, ermöglicht das System allen vollständigen Zugriff darauf.
ms.assetid: be9633fb-14ef-42d2-9269-84287b35b653
title: DACLs und ACEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28bf351fd59f634a7c7bf960aedac1c76659ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218195"
---
# <a name="dacls-and-aces"></a>DACLs und ACEs

Wenn ein Windows-Objekt nicht über eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) verfügt, ermöglicht das System allen vollständigen Zugriff darauf. Wenn ein Objekt über eine DACL verfügt, lässt das System nur den Zugriff zu, der von den [*Zugriffs Steuerungs Einträgen*](/windows/desktop/SecGloss/a-gly) (ACEs) in der DACL explizit zugelassen wird. Wenn keine ACEs in der DACL vorhanden sind, lässt das System den Zugriff auf niemanden zu. Wenn eine DACL über Aces verfügt, die den Zugriff auf eine begrenzte Gruppe von Benutzern oder Gruppen ermöglichen, verweigert das System den Zugriff auf alle Treuhänder, die nicht in den ACEs enthalten sind.

In den meisten Fällen können Sie den Zugriff auf ein Objekt mithilfe von Zugriffs zulässigen ACEs steuern. der Zugriff auf ein Objekt muss nicht explizit verweigert werden. Eine Ausnahme ist, wenn ein ACE den Zugriff auf eine Gruppe zulässt und Sie den Zugriff auf ein Mitglied der Gruppe verweigern möchten. Fügen Sie zu diesem Zweck den Benutzer "Zugriff verweigert" für den Benutzer in der DACL vor dem Access-Allowed-ACE für die Gruppe ein. Beachten Sie, dass die [Reihenfolge der ACEs](order-of-aces-in-a-dacl.md) wichtig ist, da das System die ACEs nacheinander liest, bis der Zugriff gewährt oder verweigert wird. Der ACE "Zugriff verweigert" des Benutzers muss zuerst angezeigt werden. Andernfalls wird der Zugriff auf den eingeschränkten Benutzer gewährt, wenn das System den Zugriffs zulässigen ACE der Gruppe liest.

Die folgende Abbildung zeigt eine DACL, die den Zugriff auf einen Benutzer verweigert und den Zugriff auf zwei Gruppen ermöglicht. Die Mitglieder der Gruppe A erhalten Lese-, Schreib-und Ausführungs Zugriffsrechte durch die Anhäufung der Rechte, die für die Gruppierung von A zulässig sind, sowie der Rechte, die allen Die Ausnahme ist Andrew, dem der Zugriff durch den ACE "Zugriff verweigert" verweigert wird, obwohl er kein Mitglied der Gruppe "jeder" ist.

![DACL, die unterschiedliche Zugriffsrechte basierend auf der Gruppenmitgliedschaft gewährt](images/accctrl1.png)

 

 
