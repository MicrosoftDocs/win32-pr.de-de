---
description: Konzepte der COM+-Partitionen
ms.assetid: 9fc35bef-ecc1-4764-bf69-ec89560daff4
title: Konzepte der COM+-Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 483a34e6186cda8978c1882ed1fdfbe8732f7ec8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483078"
---
# <a name="com-partitions-concepts"></a>Konzepte der COM+-Partitionen

In Computerumgebungen, in denen es erforderlich ist, unterschiedliche Versionen oder Konfigurationen einer Anwendung auf demselben Computer zu verwenden, können Konflikte auftreten, wenn eine Version der Anwendung andere Komponenten als die andere benötigt oder wenn eine Version eine Komponente auf dem Computer erfordert, die nicht mit der anderen Version der Anwendung kompatibel ist. In der Vergangenheit bestand die einzige Möglichkeit zur Lösung dieses Problems darin, mehrere Computer beizubehalten und auf jedem Computer eine andere Version der Anwendung auszuführen. Ein solcher Ansatz ist kostspielig und ineffizient, da dadurch die Hardwarekosten und der Verwaltungsaufwand erhöht werden.

Com+ löst dieses Problem durch Bereitstellen der com+-Partitions Funktion. Sie können COM+-Partitionen verwenden, um unterschiedliche Versionen einer COM+-Anwendung auf einem Computer zu installieren und diese gleichzeitig auszuführen.

Informationen zum Verständnis und zur Verwendung dieses Features finden Sie in den folgenden Themen:

-   [Was sind COM+-Partitionen?](what-are-com--partitions-.md)
-   [Partitions Implementierung](partition-implementation.md)
-   [Registrieren und Aktivieren von Komponenten in Partitionen](registering-and-activating-components-in-partitions.md)
-   [Komponenten und Partitionen in der com+-Warteschlange](com--queued-components-and-partitions.md)
-   [Einschränkungen beim Anwendungs Entwurf](application-design-restrictions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgaben für COM+-Partitionen](com--partitions-tasks.md)
</dt> </dl>

 

 



