---
description: Um die rollenbasierte Sicherheit in Ihrer COM+-Anwendung zu verwenden, müssen Sie zuerst die rollenbasierte Autorisierungsüberprüfung für die Anwendung aktivieren.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Aktivieren Role-Based Autorisierungsüberprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd46a0b09b981a3dd7731f5839458550379dad5619f22d1caaaddb24e87deaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813858"
---
# <a name="enabling-role-based-authorization-checking"></a>Aktivieren Role-Based Autorisierungsüberprüfung

Um die rollenbasierte Sicherheit in Ihrer COM+-Anwendung zu verwenden, müssen Sie zuerst die rollenbasierte Autorisierungsüberprüfung für die Anwendung aktivieren. Dadurch wird sichergestellt, dass Benutzer, die auf die Anwendung zugreifen, auf die Rolle überprüft werden, zu der sie gehören, bevor sie berechtigt sind, etwas in der Anwendung zu tun. Wenn die rollenbasierte Autorisierungsüberprüfung nicht aktiviert ist, wird die rollenbasierte Sicherheit für die Anwendung nicht verwendet.

**So aktivieren Sie die rollenbasierte Autorisierungsüberprüfung**

1.  Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die rollenbasierte Autorisierungsüberprüfung aktivieren, und klicken Sie dann auf **Eigenschaften.**

2.  Klicken Sie im Dialogfeld Anwendungseigenschaften auf die **Registerkarte Sicherheit.**

3.  Aktivieren **Sie unter Autorisierung** das Kontrollkästchen **Zugriffsüberprüfungen für diese Anwendung** erzwingen. Das Aktivieren des Kontrollkästchens bedeutet, dass die rollenbasierte Sicherheit nicht für die Anwendung verwendet wird.

4.  Klicken Sie auf **OK**.

Die ausgewählte Autorisierungseinstellung wird wirksam, wenn die Anwendung das nächste Mal gestartet wird.

 

 



