---
description: Erstellt ein Automation SafeArray mit nicht signierten Zeichen (Bytes).
ms.assetid: 67cc8cd1-95be-4498-ac25-6c418089af27
title: 'Iscardtypekonv:: kreatesafearray-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bc27a3f50f0740eca178787fd021f76c9b6729e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128096"
---
# <a name="iscardtypeconvcreatesafearray-method"></a>Iscardtypekonv:: kreatesafearray-Methode

\[Die Methode " **kreatesafearray** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die Methode " **kreatesafearray** " erstellt ein Automation SafeArray mit nicht signierten Zeichen (Bytes).

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSafeArray(
  [in]  UINT        nAllocSize,
  [out] LPSAFEARRAY *ppArray
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nzuweisung* \[ in\]
</dt> <dd>

Größe des Arbeitsspeichers in Bytes, der für das Array zugeordnet werden soll.

</dd> <dt>

*p-Ray* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das SAFEARRAY-Objekt, das zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Arbeitsspeicher wurde erfolgreich zugewiesen.<br/>                                                        |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend freier Arbeitsspeicher, um die Anforderung zu erfüllen.<br/>                                            |



 

## <a name="remarks"></a>Bemerkungen

Um ein typisches C/C++-Bytearray zu erstellen, rufen Sie " [**kreatebytearray**](iscardtypeconv-createbytearray.md)" auf.

Um einen universellen Puffer von Bytes zu erstellen, die einem **IStream** -Objekt ([**ibytebuffer**](ibytebuffer.md)) zugeordnet sind, rufen Sie " [**kreatebytebuffer**](iscardtypeconv-createbytebuffer.md)" auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scarddat. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscardtypeconfiguration**](iscardtypeconv.md)
</dt> <dt>

[Smartcard-Rückgabewerte](authentication-return-values.md)
</dt> <dt>

[**"Kreatebytearray"**](iscardtypeconv-createbytearray.md)
</dt> <dt>

[**"Kreatebytebuffer"**](iscardtypeconv-createbytebuffer.md)
</dt> </dl>

 

 
