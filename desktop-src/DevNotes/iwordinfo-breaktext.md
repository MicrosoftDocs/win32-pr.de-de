---
description: Analysiert Text, um die Wörter zu identifizieren, und stellt die Ergebnisse für das wordsink-Objekt bereit.
ms.assetid: 42bfc961-c095-4380-9b55-b58a0d9f2c00
title: 'Iwordinfo:: breaktext-Methode'
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
ms.openlocfilehash: f6f71e92137490d56c93d9443506c2d7ffa2688a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041347"
---
# <a name="iwordinfobreaktext-method"></a>Iwordinfo:: breaktext-Methode

\[Diese Methode ist veraltet und wird unter Windows Vista nicht unterstützt.\]

Analysiert Text, um die Wörter zu identifizieren, und stellt die Ergebnisse für das [wordsink](/previous-versions//ms691570(v=vs.85)) -Objekt bereit.

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

*ptextsource* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [Text \_ Quellen](/previous-versions//ms690919(v=vs.85)) Struktur, die den Unicode-Text enthält.

</dd> <dt>

*pwordsink* \[ in\]
</dt> <dd>

Ein Zeiger auf das [wordsink](/previous-versions//ms691570(v=vs.85)) -Objekt, das die von dieser Methode generierten Wörter empfängt und verarbeitet. Wenn dieser Parameter **null** ist, unterbricht die Methode die Zeichenfolge nicht in Wörter.

</dd> <dt>

Modus "f"  \[ in\]
</dt> <dd>

Der Break-Modus. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="IWORDINFO_BREAKTEXTMODE_DICTFORM"></span><span id="iwordinfo_breaktextmode_dictform"></span><dl> <dt>**Iwordinfo \_ Breaktextmode- \_ Wörter Form**</dt> <dt>0x00000002</dt> </dl> | Word unterbrechen die Text Zeichenfolge und übergeben das Wörterbuch Formular der Wörter an das **wordsink** -Objekt.<br/> |
| <span id="IWORDINFO_BREAKTEXTMODE_SMARTSEL"></span><span id="iwordinfo_breaktextmode_smartsel"></span><dl> <dt>**Iwordinfo \_ Breaktextmode \_ smartsel**</dt> <dt>0x00000001</dt> </dl> | Word unterbricht die Text Zeichenfolge und übergibt die Wörter an das **wordsink** -Objekt.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                            | Beschreibung                                                                                             |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Der Vorgang wurde erfolgreich ausgeführt. Zum Auffüllen des *ptextsource* -Puffers steht kein Text mehr zur Verfügung.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Der *ptextsource* -Parameter ist **null**.<br/>                                                     |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie das **pfnfilltextbuffer** -Element der **Text \_ Quellen** Struktur, um den Quelltext aufzufüllen. Diese Methode muss alle Rückgabewerte der **pfnfilltextbuffer** -Rückruffunktion verarbeiten. Wenn ein Fehler auftritt, beenden Sie die Verarbeitung des Texts im Puffer, bevor Sie den Fehler behandeln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwordinfo**](iwordinfo.md)
</dt> <dt>

[Text \_ Quelle](/previous-versions//ms690919(v=vs.85))
</dt> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[Wordsink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
