---
description: Analysiert Text, um Wörter zu identifizieren, und stellt die Ergebnisse für das WordSink-Objekt zur Wahl.
ms.assetid: 42bfc961-c095-4380-9b55-b58a0d9f2c00
title: IWordInfo::BreakText-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 4cb4e4b27b52a4fb22a65f382a20c51a43ca5c77feb14828a7ea252e75c3b0f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749740"
---
# <a name="iwordinfobreaktext-method"></a>IWordInfo::BreakText-Methode

\[Diese Methode ist veraltet und wird auf Windows Vista nicht unterstützt.\]

Analysiert Text, um Wörter zu identifizieren, und stellt die Ergebnisse für das [WordSink-Objekt](/previous-versions//ms691570(v=vs.85)) zur Wahl.

## <a name="syntax"></a>Syntax


```C++
HRESULT BreakText(
  [in] TEXT_SOURCE *pTextSource,
  [in] IWordSink   *pWordSink,
  [in] DWORD       fBreakMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTextSource* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [TEXT \_ SOURCE-Struktur,](/previous-versions//ms690919(v=vs.85)) die den Unicode-Text enthält.

</dd> <dt>

*pWordSink* \[ In\]
</dt> <dd>

Ein Zeiger auf das [WordSink-Objekt,](/previous-versions//ms691570(v=vs.85)) das die von dieser Methode generierten Wörter empfängt und behandelt. Wenn dieser Parameter **NULL ist,** unterbricht die Methode die Zeichenfolge nicht in Wörter.

</dd> <dt>

*fBreakMode* \[ In\]
</dt> <dd>

Der Unterbrechungsmodus. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="IWORDINFO_BREAKTEXTMODE_DICTFORM"></span><span id="iwordinfo_breaktextmode_dictform"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ DICTFORM-0x00000002**</dt> <dt></dt> </dl> | Durch wörterbrechen Sie die Textzeichenfolge, und übergeben Sie die Wörterbuchform der Wörter an das **WordSink-Objekt.**<br/> |
| <span id="IWORDINFO_BREAKTEXTMODE_SMARTSEL"></span><span id="iwordinfo_breaktextmode_smartsel"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ SMARTSEL-0x00000001**</dt> <dt></dt> </dl> | Word bricht die Textzeichenfolge auf und übergibt die Wörter an das **WordSink-Objekt.**<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                            | Beschreibung                                                                                             |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Der Vorgang wurde erfolgreich ausgeführt. Es ist kein Text mehr verfügbar, um den *pTextSource-Puffer erneut* aufzufüllen.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Der *pTextSource-Parameter* ist **NULL.**<br/>                                                     |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie **das pfnFillTextBuffer-Member** der **TEXT \_ SOURCE-Struktur,** um den Quelltext aufzufüllen. Diese Methode muss alle Rückgabewerte der **Rückruffunktion pfnFillTextBuffer** verarbeiten. Wenn ein Fehler auftritt, beenden Sie die Verarbeitung des Texts im Puffer, bevor Sie den Fehler behandeln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWordInfo**](iwordinfo.md)
</dt> <dt>

[\_TEXTQUELLE](/previous-versions//ms690919(v=vs.85))
</dt> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
