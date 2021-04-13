---
description: 'Tritt auf, wenn die iinkanalyzer:: Analysis-Methode oder die iinkanalyzer:: BackgroundAnalyze-Methode aufgerufen wird.'
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: '_IAnalysisEvents:: Activity-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f235d3414b0d514f32b4ebd197c04a8721968a2a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351818"
---
# <a name="_ianalysiseventsactivity-event"></a>\_Ianalysil Vents:: Activity-Ereignis

Tritt auf, wenn die [**iinkanalyzer:: Analysis**](iinkanalyzer-analyze.md) -Methode oder die [**iinkanalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) -Methode aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Activity();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis zeigt an, dass [**iinkanalyzer**](iinkanalyzer.md) eine Handschrift Analyse ausführt. Dieses Ereignis weist nicht auf den Fortschritt des frei Hand Analyse Vorgangs hin.

Implementieren Sie einen **\_ ianalysilvents:: Activity** -Ereignishandler, um einen der folgenden Schritte durchführen zu können:

-   Geben Sie dem Benutzer an, dass die Handschrift Analyse durchgeführt wird.
-   Benutzereingaben während synchroner Analyse verarbeiten.
-   Empfangen von Benachrichtigungen über Systemanforderungen, z. b. das Neuzeichnen des Anwendungsfensters während der frei Hand Analyse.

Der [**iinkanalyzer**](iinkanalyzer.md) löst dieses Ereignis häufig während der Layoutanalysephase und der Erstellungsphase für die Erstellung und Zeichnung der frei Hand Analyse aus. Der **iinkanalyzer** löst dieses Ereignis während der Handschrift Erkennungs Phase vor und nach dem Zugriff auf eine frei Handerkennung aus.

Die Anzahl der Aktivitäts Ereignisse, die von [**iinkanalyzer**](iinkanalyzer.md) generiert werden, ist betroffen von:

-   Die frei Handerkennung, die der [**iinkanalyzer**](iinkanalyzer.md) für die frei Handerkennung anwendet.
-   Die Anzahl und Länge der Striche, die von [**iinkanalyzer**](iinkanalyzer.md) analysiert werden.
-   Die Anzahl der Striche, die als Schreibvorgänge klassifiziert werden.

Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_Ianalysil Vents**](-ianalysisevents.md)
</dt> <dt>

[**\_Ianalysisproxyevents**](-ianalysisproxyevents.md)
</dt> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalysiserkenzer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




