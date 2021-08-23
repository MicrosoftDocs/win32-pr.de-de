---
description: Die Seek-Methode wählt das Objekt aus, aus dem (Lese-/Schreibzugriff) erfolgen soll.
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: ISCardFileAccess::Seek-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5f4059eb2943411cfa5a3fb2b2ae247cd0fda7dd735cc1f1f61d516181976b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923159"
---
# <a name="iscardfileaccessseek-method"></a>ISCardFileAccess::Seek-Methode

\[Die **Seek-Methode** ist für die Verwendung in den betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **Seek-Methode** wählt das Objekt aus, aus dem (Lese-/Schreibzugriff) erfolgen soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFile* \[ In\]
</dt> <dd>

Handle der geöffneten Datei.

</dd> <dt>

*Seek* \[ In\]
</dt> <dd>

Der Ort, an dem die Suche beginnen soll.



| Wert                                                                                                | Bedeutung                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>SC \_ SEEK VON ANFANG \_ \_ AN</dt> </dl> | Beginnen Sie am Anfang mit der Suche.<br/>          |
| <dl> <dt>SC \_ SEEK \_ FROM \_ END </dt> </dl>      | Beginnen Sie die Suche am Ende.<br/>              |
| <dl> <dt>SC \_ SEEK \_ RELATIVE</dt> </dl>        | Beginnen Sie die Suche von der aktuellen Position aus.<br/> |



 

</dd> <dt>

*lOffset* \[ In\]
</dt> <dd>

Anzahl der Datenobjekte aus dem Verweisobjekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Um eine Datei zu lesen oder aus einer Datei zu schreiben, rufen [**Sie Lesen**](iscardfileaccess-read.md) bzw. [**Schreiben**](iscardfileaccess-write.md) auf.

Eine Liste aller von dieser Schnittstelle definierten Methoden finden Sie unter [**ISCardFileAccess**](iscardfileaccess.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcardfehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**Überwachungsdaten**](iscardfileaccess-read.md)
</dt> <dt>

[**Schreiben**](iscardfileaccess-write.md)
</dt> </dl>

 

 
