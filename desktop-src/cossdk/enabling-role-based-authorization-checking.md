---
description: Um die rollenbasierte Sicherheit in der com+-Anwendung zu verwenden, müssen Sie zunächst die rollenbasierte Autorisierungs Überprüfung für die Anwendung aktivieren.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Aktivieren der Role-Based Autorisierungs Überprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4268c35812af04ed8a0056900e821029274756
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041470"
---
# <a name="enabling-role-based-authorization-checking"></a>Aktivieren der Role-Based Autorisierungs Überprüfung

Um die rollenbasierte Sicherheit in der com+-Anwendung zu verwenden, müssen Sie zunächst die rollenbasierte Autorisierungs Überprüfung für die Anwendung aktivieren. Dadurch wird sichergestellt, dass Benutzer, die auf die Anwendung zugreifen, auf die Rolle geprüft werden, der Sie angehören, bevor Sie autorisiert werden, etwas in der Anwendung durchzuführen. Wenn die rollenbasierte Autorisierungs Überprüfung nicht aktiviert ist, wird die rollenbasierte Sicherheit für die Anwendung nicht verwendet.

**So aktivieren Sie die rollenbasierte Autorisierungs Überprüfung**

1.  Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie die rollenbasierte Autorisierungs Überprüfung aktivieren, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .

3.  Wählen Sie unter **Autorisierung** das Kontrollkästchen **Zugriffs Überprüfungen für diese Anwendung erzwingen aus** . Das Deaktivieren des Kontrollkästchens bedeutet, dass für die Anwendung keine rollenbasierte Sicherheit verwendet wird.

4.  Klicken Sie auf **OK**.

Die ausgewählte Autorisierungs Einstellung wird wirksam, wenn die Anwendung das nächste Mal gestartet wird.

 

 



