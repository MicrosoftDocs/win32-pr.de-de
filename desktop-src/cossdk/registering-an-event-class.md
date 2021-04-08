---
description: Damit Abonnenten eine Ereignisklasse finden und Sie abonnieren können, müssen Ereignis Klassen im com+-Katalog registriert werden.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Registrieren einer Ereignisklasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748289"
---
# <a name="registering-an-event-class"></a>Registrieren einer Ereignisklasse

Damit Abonnenten eine Ereignisklasse finden und Sie abonnieren können, müssen Ereignis Klassen im com+-Katalog registriert werden. Com+ erfordert eine Typbibliothek, die die Ereignis Schnittstellen und Methoden beschreibt, damit Sie Abonnenten und Verleger ordnungsgemäß abgleichen und verbinden können. Die Typbibliothek muss sich in einer selbst Registrierungs-DLL befinden oder von ihr begleitet werden.

Sie können das Verwaltungs Programmkomponenten Dienste oder die administrativen com+-Funktionen verwenden, um eine Ereignisklasse im com+-Katalog zu registrieren.

**So registrieren Sie eine Ereignisklasse beim Verwaltungs Programm "Komponenten Dienste"**

1.  Erstellen Sie eine neue COM+-Anwendung.

2.  Öffnen Sie den Anwendungsordner, und wählen Sie **Komponenten** aus.

3.  Klicken Sie im Menü **Aktion** auf **Neu**. (Sie können auch den Ordner **Komponenten** auswählen, mit der rechten Maustaste klicken, auf **neu** zeigen und dann auf **Komponente** klicken.)

4.  Klicken Sie auf **neue Ereignisklasse installieren**.

5.  Geben Sie den Pfad zur Komponenten-DLL der Ereignisklasse ein.

6.  Klicken Sie auf **OK**.

Die Ereignisklasse wird im com+-Katalog registriert und kann von Abonnenten gefunden werden, die an der Beschaffung der von der Ereignisklasse bereitgestellten Informationen interessiert sind. Informationen zum Registrieren der Ereignisklasse mithilfe der com+-Verwaltungs Schnittstellen finden Sie unter [**icomadmincatalog:: installeventclass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren eines Abonnements](registering-a-subscription.md)
</dt> </dl>

 

 



