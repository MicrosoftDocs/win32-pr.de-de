---
description: Die Implementierung dieser Schnittstelle wird als Beispielcode mit dem DirectShow SDK bereitgestellt.
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: IMpeg2PsiParser-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342720"
---
# <a name="impeg2psiparser-interface"></a>IMpeg2PsiParser-Schnittstelle

Die Implementierung dieser Schnittstelle wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die- `IMpeg2PsiParser` Schnittstelle ruft Programm spezifische Informationen (PSI) aus dem PSI-Parser-Filter ab, der im DirectShow SDK als Beispiel Filter bereitgestellt wird. Eine Anwendung kann diesen Filter verwenden, um Programm-IDs (PIDs) dem MPEG-2-Demultiplexer-Filter zuzuordnen.

## <a name="members"></a>Member

Die **IMpeg2PsiParser** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IMpeg2PsiParser** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IMpeg2PsiParser** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                             | BESCHREIBUNG                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**Findrecordprogrammappid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))         | Sucht die PMT-PID (Program Map Table) für ein Programm, sofern die Programmnummer angegeben ist.<br/> |
| [**Getzähltofelementarystreams**](impeg2psiparser-getcountofelementarystreams.md) | Ruft die Anzahl der elementaren Datenströme in einem angegebenen Programm ab.<br/>             |
| [**Getgräfin-Druck Programme**](impeg2psiparser-getcountofprograms.md)                   | Ruft die Anzahl der Programme im Transportstream ab.<br/>                      |
| [**Getpatversionnumber**](impeg2psiparser-getpatversionnumber.md)                 | Ruft das Feld mit der Versions \_ Nummer aus der Programm Zuordnungs Tabelle (Pat) ab.<br/>  |
| [**Getpmtversionnumber**](impeg2psiparser-getpmtversionnumber.md)                 | Ruft das Feld der Versions \_ Nummer von einem angegebenen PMT ab.<br/>                      |
| [**Getrecorschementarypid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))           | Ruft die PID-Zuweisung für einen angegebenen elementaren Stream in einem Programm ab.<br/>   |
| [**Getrecordprogrammappid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))           | Ruft die PID-Zuweisung für ein angegebenes PMT ab.<br/>                              |
| [**Getrecordprogramnumber**](impeg2psiparser-getrecordprogramnumber.md)           | Ruft die Programmnummer für ein angegebenes Programm ab.<br/>                          |
| [**Getrecordstreamtype**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))                 | Ruft den Streamtyp für einen angegebenen elementaren Stream in einem Programm ab.<br/>      |
| [**Gettransportstreamid**](impeg2psiparser-gettransportstreamid.md)               | Ruft das Transportdaten \_ Strom- \_ ID-Feld aus der PAT-Datei ab.<br/>                        |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beispiel für PSI-Parser-Filter](psi-parser-filter-sample.md)
</dt> </dl>

 

 
