---
description: Als Teil der durch TSPI definierten Telefongeräte Abstraktion muss TAPI und der Dienstanbieter zunächst die grundlegende Initialisierung durchlaufen.
ms.assetid: cd8bb328-fbd0-409c-8471-34ad4c2c8d93
title: Telefon-SPI-Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0c54e313c2be3846aeb604217f5324ec0d8a8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373187"
---
# <a name="phone-spi-initialization"></a>Telefon-SPI-Initialisierung

Als Teil der durch TSPI definierten Telefongeräte Abstraktion muss TAPI und der Dienstanbieter zunächst die grundlegende Initialisierung durchlaufen. Diese grundlegende Initialisierung wird sowohl für die Linie als auch die Telefon Hälfte der Schnittstelle durch denselben Satz von Schritten erreicht. Der erste Schritt ist die Aushandlung der Schnittstellen Version. TAPI führt dies durch Aufrufen der [**TSPI \_ linenegotiatetspiversion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) -Funktion durch. Diese Funktion wird normalerweise verwendet, um im Auftrag eines einzelnen Zeilen Geräts zu verhandeln. verschiedene Linien Geräte innerhalb desselben Dienstanbieters funktionieren möglicherweise entsprechend den verschiedenen Schnittstellen Versionen. TAPI übergibt einen speziellen Wert für den reservierten Geräte Bezeichner, [**initialisieren Sie die \_ Aushandlung**](initialize-negotiation.md), um anzugeben, dass er eine allgemeine Schnittstellen Version für Initialisierungs Funktionen aushandelt, die den gesamten Dienstanbieter betreffen, sowohl für Zeilen als auch für Telefone.

Das Ergebnis dieser Aushandlung wird an nachfolgende Prozeduren zurückgegeben, bis ein Telefongerät geöffnet wird. Zu diesem Zeitpunkt wird das Telefongerät an eine bestimmte Schnittstellen Version übertragen. Diese Schnittstellen Version ist implizit, bis das Telefon geschlossen wird. Sie muss nicht an nachfolgende Funktionen weitergeleitet werden, die auf einem geöffneten Telefon ausgeführt werden.

Nach der allgemeinen Aushandlung der Schnittstellen Version ruft TAPI die [**TSPI \_ providerinit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) -Funktion auf. Diese Funktion initialisiert den Dienstanbieter und gibt ihm außerdem Parameter, die für den nachfolgenden Vorgang erforderlich sind. Diese Parameter umfassen Folgendes:

-   *dwpermanentproviderid*: gibt den permanenten Bezeichner des zu initialisierenden Dienstanbieters an, der innerhalb der Dienstanbieter auf diesem System eindeutig ist.
-   *dwlinedeviceidbase*: gibt den niedrigsten Geräte Bezeichner für die Linien Geräte an, die von diesem Dienstanbieter unterstützt werden.
-   *dwphonedeviceidbase*: gibt den niedrigsten Geräte Bezeichner für die von diesem Dienstanbieter unterstützten Telefongeräte an. Geräte der telefoniegeräterklasse werden durch ganze Zahlen identifiziert, beginnend bei Null. Dieser Bereich von bezeichaten ist in allen Telefongeräten zusammenhängend. Da es möglicherweise mehrere Dienstanbieter gibt, die Telefongeräte in einem einzelnen System verwalten, erhält jeder Dienstanbieter einen zusammenhängenden Teil des Gesamtbereichs. Dieser Parameter weist den Dienstanbieter an, den niedrigsten Wert im Bereich des Bereichs zu haben. Der Dienstanbieter ist für die Zuordnung dieses Variablen Bereichs zu seinen eigenen internen Geräte bezeichlern verantwortlich. Dadurch erhält der Anbieter des Dienstanbieters ausreichend Flexibilität, Geräte Bezeichner in gerätespezifischen Erweiterungen zu verwenden, wenn er dies möchte. Da der Dienstanbieter weiß, welche Geräte Bezeichner in TAPI-definierten Parametern und Datenstrukturen angezeigt werden, kann er konsistente Geräte Bezeichner in gerätespezifischen Erweiterungs Parametern und Datenstrukturen verwenden.
-   *dwnumlines*: gibt die Anzahl von Zeilen Geräten an, die dieser Dienstanbieter unterstützt.
-   *dwnumphones*: gibt an, wie viele Telefongeräte dieser Dienstanbieter unterstützt.
-   *lpfncompletionproc*: gibt die Prozedur an, die der Dienstanbieter aufruft, um den Abschluss aller asynchronen Betriebs Prozeduren auf Zeilen-und Telefongeräten zu melden.

Nach [**TSPI \_ providerinit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)können normale Vorgänge (z. b. das Öffnen von Telefonen) ausgeführt werden.

 

 
