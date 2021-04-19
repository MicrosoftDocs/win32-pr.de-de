---
description: Akkus können Stromversorgung für tragbare Computer und Computer bereitstellen, die auf einer unterbrechungsfreien Stromversorgung (USV) ausgeführt werden.
ms.assetid: 3580b37d-611c-46b4-9300-4943833d6852
title: Akku Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f9838a2a95db037b9655f116f07e3cf2e072d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368745"
---
# <a name="battery-information"></a>Akku Informationen

Akkus können Stromversorgung für tragbare Computer und Computer bereitstellen, die auf einer unterbrechungsfreien Stromversorgung (USV) ausgeführt werden. Auf diesen Computern bietet das Betriebssysteminformationen zum Zustand des Akkus, damit Anwendungen nützliche Funktionen für den Benutzer bereitstellen können. (Einige ältere nicht standardmäßige Akku Systeme und UPSS werden nicht unterstützt.)

Beachten Sie, dass diese Übersicht voraussetzt, dass Sie mit der [Geräteverwaltung](/windows/desktop/DevIO/device-management)vertraut sind.

Um Informationen zum Akku Status zu erhalten, verwenden Sie die [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) -Funktion, die allgemeine Informationen zu allen Stromquellen im System zurückgibt. Sie sollten **GetSystemPowerStatus** nach Möglichkeit verwenden.

In einigen Fällen sind jedoch ausführliche Informationen zu den einzelnen Akkus erforderlich. Zu diesem Zweck macht jedes Akku Gerät eine ioctl-Schnittstelle verfügbar. Die folgenden ioctl-Vorgänge werden mithilfe der [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion ausgeführt:

<dl>

[**IOCTL- \_ Akku \_ Abfrage \_ Informationen**](ioctl-battery-query-information.md)  
[**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md)  
[**IOCTL \_ Akku \_ - \_ abfragetag**](ioctl-battery-query-tag.md)  
[**IOCTL- \_ Akku \_ Satz \_ Informationen**](ioctl-battery-set-information.md)  
</dl>

Um diese Schnittstelle zu verwenden, muss eine Anwendung mehreren Schritten folgen. Zuerst müssen Setup Routinen verwendet werden, um alle Geräte aufzulisten, die über eine Akku Klassen Schnittstelle verfügen. Beachten Sie, dass diese Geräte die Akku Anschlüsse und nicht die tatsächlich im System vorhandenen Akkus darstellen. Die Anwendung muss dann ein Handle für jedes Gerät öffnen, damit Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) verwenden kann, um Anforderungen an das Gerät zu senden, und dann Tags für alle Akkus abrufen, die eingefügt werden. Nachdem Sie diese Schritte ausgeführt haben, kann die Anwendung Abfragen an die einzelnen Akku Geräte senden.

## <a name="battery-tags"></a>Akku-Tags

Da jedes Akku Gerät einen Slot darstellt, in den ein Akku eingefügt werden kann, muss es eine Möglichkeit geben, zu bestimmen, wann der Akku entfernt und erneut eingefügt, ersetzt oder geändert wird. Zu diesem Zweck wird jedem Akku in einem bestimmten Slot ein Tag zugewiesen. Dieses Tag muss für alle Abfragen nach Informationen verwendet werden. Wenn das von der Anwendung bereitgestellte Tag nicht mit dem Akku identisch ist, schlägt die Abfrage fehl, was der Anwendung anzeigt, dass sich der Akku auf irgendeine Weise geändert hat. Zum erfolgreichen Abschluss der Abfrage ist ein neues Akku Kennzeichen erforderlich. Erwerben Sie das Tag mithilfe des [**IOCTL- \_ \_ abfragetagvorgangs \_**](ioctl-battery-query-tag.md) . Wenn ein Akku in diesem Slot vorhanden ist, kann das zurückgegebene Tag an jeden anderen Akku-IOCTLs zum Ausführen anderer Funktionen übermittelt werden. Auf einem System mit mehreren Akkus gibt jedes Akku Gerät (Slot) Akku Tags unabhängig aus, sodass das Tag von zwei separaten Geräten manchmal identisch sein könnte.

Eine Änderung im Akku-Tag bedeutet nicht notwendigerweise, dass der Akku entfernt und erneut eingefügt oder ersetzt wurde. Ein neues Tag kann generiert werden, wenn eine Änderung in einem der Daten vorliegt, die normalerweise statisch wäre. Wenn z. b. die Abrechnung für einen Akku abgeschlossen ist, hat sich möglicherweise die letzte vollständig berechnete Kapazität geändert. Das Tag kann sich auch ändern, wenn die Akku Kommunikation vorübergehend unterbrochen wurde oder wenn eine falsche Benachrichtigung vom BIOS aufgetreten ist. Auf einigen Systemen kann das Akku Kennzeichen immer dann aktualisiert werden, wenn sich der AC-Status ändert. Dieses Verhalten ist auf ein Merkmal des Akku Systems zurückzuführen und nicht üblich.

Wenn das Akku Kennzeichen aktualisiert wird, sollte der Akku so behandelt werden, als ob es sich um einen neuen Akku handelt und alle zwischengespeicherten Daten erneut gelesen werden sollen. Wenn eine Anwendung wissen muss, ob dieselbe physische Akkukapazität vorhanden ist, sollte Sie den Wert von " **batteryuniqueid** " im Ausgabepuffer der [**IOCTL- \_ Akku \_ Abfrage \_ Informationen**](ioctl-battery-query-information.md) überprüfen, wenn Sie mit der Informationen auf der Ebene " **batteryuniqueid** " aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energie Verwaltung](about-power-management.md)
</dt> <dt>

[Aufzählen von Akku Geräten](enumerating-battery-devices.md)
</dt> </dl>

 

 
