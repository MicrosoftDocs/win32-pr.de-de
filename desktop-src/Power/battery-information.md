---
description: Akkus können Stromversorgung für tragbare Computer und Computer bereitstellen, die mit einer unterbrechungsfreie Stromversorgung (USV) ausgeführt werden.
ms.assetid: 3580b37d-611c-46b4-9300-4943833d6852
title: Akkuinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b1afd2461985ec85a07d40bd309c588a5404e4b59be7555a01fc6c147eb221
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143693"
---
# <a name="battery-information"></a>Akkuinformationen

Akkus können Stromversorgung für tragbare Computer und Computer bereitstellen, die mit einer unterbrechungsfreie Stromversorgung (USV) ausgeführt werden. Auf diesen Computern stellt das Betriebssystem Informationen zum Zustand des Akkus zur Verfügung, damit Anwendungen nützliche Funktionen für den Benutzer bereitstellen können. (Einige ältere, nicht standardmäßige Akkusysteme und UPS werden nicht unterstützt.)

Beachten Sie, dass in dieser Übersicht davon ausgegangen wird, dass Sie mit der [Geräteverwaltung vertraut sind.](/windows/desktop/DevIO/device-management)

Um Informationen zum Akkustatus zu erhalten, verwenden Sie die [**GetSystemPowerStatus-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) die allgemeine Informationen zu allen Stromquellen im System zurückgibt. Verwenden Sie nach Möglichkeit **GetSystemPowerStatus.**

In einigen Fällen sind jedoch ausführliche Informationen zu den einzelnen Akkus erforderlich. Zu diesem Zweck macht jedes Akkugerät eine IOCTL-Schnittstelle verfügbar. Die folgenden IOCTL-Vorgänge werden mithilfe der [**DeviceIoControl-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ausgeführt:

<dl>

[**IOCTL \_ BATTERY \_ QUERY \_ INFORMATION**](ioctl-battery-query-information.md)  
[**IOCTL \_ BATTERY \_ QUERY \_ STATUS**](ioctl-battery-query-status.md)  
[**IOCTL \_ BATTERY \_ QUERY \_ TAG**](ioctl-battery-query-tag.md)  
[**\_IOCTL-AKKUSATZINFORMATIONEN \_ \_**](ioctl-battery-set-information.md)  
</dl>

Um diese Schnittstelle zu verwenden, muss eine Anwendung mehrere Schritte ausführen. Zunächst müssen Setuproutinen verwendet werden, um alle Geräte mit einer Akkuklassenschnittstelle aufzählen zu können. Beachten Sie, dass diese Geräte die Akkuports darstellen, nicht die tatsächlichen Akkus, die im System vorhanden sind. Die Anwendung muss dann ein Handle für jedes Gerät öffnen, damit sie die [**DeviceIoControl-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) verwenden kann, um Anforderungen an das Gerät zu senden und dann Tags für alle eingefügten Akkus zu erhalten. Nach Abschluss dieser Schritte kann die Anwendung Abfragen an jedes Akkugerät senden.

## <a name="battery-tags"></a>Akkutags

Da jedes Akkugerät einen Einschub darstellt, in den ein Akku eingefügt werden kann, muss es eine Möglichkeit geben, zu bestimmen, wann der Akku entfernt und erneut ein- oder aus ausgetauscht oder auf andere Weise geändert wird. Zu diesem Grund wird jedem Akku in einem bestimmten Einschub ein Tag zugewiesen. Dieses Tag muss für alle Abfragen verwendet werden, um Informationen zu erhalten. Wenn das von der Anwendung bereitgestellte Tag nicht mit dem Akku passt, schlägt die Abfrage fehl und gibt der Anwendung an, dass sich der Akku in irgendeiner Weise geändert hat. Um die Abfrage erfolgreich abschließen zu können, ist ein neues Akkutag erforderlich. Erwerben Sie das Tag mithilfe [**des IOCTL \_ BATTERY QUERY \_ \_ TAG-Vorgangs.**](ioctl-battery-query-tag.md) Wenn in diesem Slot ein Akku vorhanden ist, kann das zurückgegebene Tag an eine der anderen Akku-IOCTLs übergeben werden, um andere Funktionen auszuführen. Bei einem Mehrakkusystem gibt jedes Akkugerät (Einschubfach) unabhängig Akkutags aus, sodass das Tag von zwei separaten Geräten manchmal identisch sein kann.

Eine Änderung des Akkutags bedeutet nicht notwendigerweise, dass der Akku entfernt und erneut ein- oder ausgetauscht wurde. Ein neues Tag kann generiert werden, wenn eine Änderung an daten vor sich geht, die normalerweise statisch wäre. Wenn beispielsweise ein Akku geladen wird, hat sich die letzte vollständig geladene Kapazität möglicherweise geändert. Das Tag kann sich auch ändern, wenn die Akkukommunikation vorübergehend unterbrochen wurde oder eine falsche Benachrichtigung vom BIOS vorging. In einigen Systemen kann das Akkutag aktualisiert werden, wenn sich der Ac-Status ändert. Dieses Verhalten ist auf ein Merkmal des Akkusystems und nicht üblich.

Wenn das Akkutag aktualisiert wird, sollte der Akku so behandelt werden, als wäre er ein neuer Akku, und alle zwischengespeicherten Daten sollten erneut gelesen werden. Wenn eine Anwendung wissen muss, ob der gleiche physische Akku vorhanden ist, sollte sie den Wert **von BatteryUniqueID** im Ausgabepuffer von [**IOCTL \_ BATTERY QUERY \_ \_ INFORMATION**](ioctl-battery-query-information.md) überprüfen, wenn sie mit der **BatteryUniqueID-Informationsebene** aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energieverwaltung](about-power-management.md)
</dt> <dt>

[Aufzählen von Akkugeräten](enumerating-battery-devices.md)
</dt> </dl>

 

 
