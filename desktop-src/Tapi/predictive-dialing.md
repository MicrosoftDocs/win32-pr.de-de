---
description: Die Vorhersage Wahl ist eine Anwendung, die in der Regel auf einem Callcenter-Telefonserver ausgeführt wird.
ms.assetid: c8d0b2b5-61eb-4ab0-b09d-c54c282b730e
title: Vorhersagbare Wahl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576ebffff5d4b9925fd50ecce082e4f515065c5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351419"
---
# <a name="predictive-dialing"></a>Vorhersagbare Wahl

Die Vorhersage Wahl ist eine Anwendung, die in der Regel auf einem Callcenter-Telefonserver ausgeführt wird. Es wird eine Liste von Telefonnummern verwendet, die häufig aus einer Datenbank abgerufen werden, um ausgehende Anrufe zu versuchen. Wenn ein-Befehl *abgeschlossen* ist, wird der-Befehl automatisch einem Agent zur Verarbeitung zugewiesen. Die Anwendung kann einen *vorher sagewählbaren Port* für einen Switch verwenden, bei dem es sich um ein Gerät handelt, das ausgehende Aufrufe ausführen kann und über besondere Fähigkeiten verfügt (durch DSP usw.), um Aufruf Status Töne und andere akustische Anzeichen des Aufruf Zustands zu erkennen. Wenn ein Ansichts Ansichts Port aufgerufen wird, wird er in der Regel automatisch auf ein anderes Gerät auf dem Switch übertragen, wenn der-Befehl einen bestimmten Zustand erreicht, oder wenn ein bestimmter Medientyp erkannt wird. Dieses Zielgerät kann eine Warteschlange für Agents sein, die ausgehende Aufrufe verarbeiten.

Anwendungen identifizieren ein Gerät als Funktion der Vorhersage Wahl durch das lineaddrcapflags \_ predictivedialer-Bit im **dwaddrcapflags** -Member in [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps). Der Member " **dwpredictiveautotransferstates** " in **lineaddresscaps** gibt die Zustände an, für die der Vorhersage-eingabeport für die automatische Übertragung eines Aufrufes befohlen werden kann. Wenn dieser Member 0 (null) ist, bedeutet dies, dass keine automatische Übertragung verfügbar ist und dass die Anwendung Aufrufe explizit übertragen muss, wenn der entsprechende Aufruf Zustand (oder der Medientyp oder andere Kriterien) erkannt wird. Vorzugsweise können Switchhersteller sowohl automatische als auch manuelle Übertragungen verfügbar machen und Anwendungen die Auswahl des bevorzugten Mechanismus ermöglichen, aber Dienstanbieter müssten das Verhalten der Legacy Geräte modellieren. Ein einzelner vorhersag barer Wähl Anschluss (Line Device/Address) kann das Ausführen mehrerer ausgehender Aufrufe gleichzeitig unterstützen, wie vom **dwmaxnumactivecalls** -Member in **lineaddresscaps** angegeben. Die Funktion zur Vorhersage von Wahlmöglichkeiten kann auch auf jedem Gerät verfügbar gemacht werden. dabei wird ein gemeinsam genutzter Pool von Signalprozessoren für die Vorhersage Wahl verwendet, die auf die Zeile überbrückt werden, die auf Anforderung gewählt wird.

Wenn die [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) -Funktion für eine Linie verwendet wird, die eine Vorhersage Wahl ermöglicht (ein Port mit dem lineaddrcapflags \_ predictivedialer-Satz) und die Vorhersage Wahl mithilfe von linecallparamflags \_ predictivedial angefordert wird, wird der Anruf in einer Vorhersage Weise mit erweiterter, hörender Status Erkennung ausgeführt. Zusätzliche Felder und Konstanten werden in der [**linecallpara**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) -Struktur definiert, die an **linemakecall** übergeben wird, um das Verhalten des vorhersagbaren Wähl Anschlusses zu steuern. Das Element " **dwpredictiveautotransferstates** " gibt den Zeilen Aufruf an, dass der Vorhersage-Port nach dem Aufruf eines beliebigen Werts automatisch den Aufruf an das angegebene Ziel übertragen soll (die Bits müssen eine ordnungsgemäße Teilmenge der unterstützten automatischen Übertragungs Zustände sein, die in [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)angegeben sind). die Anwendung kann das Feld auf 0 (null) belassen, wenn Sie die Aufrufe selbst überwachen und den Befehl mithilfe von [**lineblintransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer) übertragen soll, wenn die gewünschte Bedingung erreicht wird. Die Anwendung muss die gewünschte Adresse angeben, an die der Aufruf automatisch in dem Variablen Feld übertragen werden soll, das durch die **dwtargetaddresssize** -und **dwtargetaddressoffset** -Member in **linecallparser** definiert wird.

Anwendungen können auch ein Timeout für ausgehende Aufrufe festlegen, sodass der Dienstanbieter diese automatisch in einen getrennten Status übergeht, wenn Sie nicht beantwortet werden. Dies wird mit dem **dwnobeantwortimeout** -Member in [**linecallpara**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)Metern gesteuert.

 

 



