---
description: Die Seek-Methode wählt das Objekt aus, von dem aus der Zugriff (Lese-/Schreibzugriff) erfolgen soll.
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: 'Iscardfileaccess:: Seek-Methode'
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
ms.openlocfilehash: c0d23925ba1c38a05e15bea5e6ee63b3a1c87125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756882"
---
# <a name="iscardfileaccessseek-method"></a>Iscardfileaccess:: Seek-Methode

\[Die **Seek** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Seek** -Methode wählt das Objekt aus, von dem aus der Zugriff (Lese-/Schreibzugriff) erfolgen soll.

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

*hFile* \[ in\]
</dt> <dd>

Handle der geöffneten Datei.

</dd> <dt>

*Suchen* \[ in\]
</dt> <dd>

Der Speicherort, an dem der Suchvorgang beginnen soll.



| Wert                                                                                                | Bedeutung                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>SC- \_ Suche \_ von \_ Anfang an</dt> </dl> | Beginnen Sie mit der Suche am Anfang.<br/>          |
| <dl> <dt>SC- \_ Suche \_ von \_ Ende </dt> </dl>      | Starten Sie die Suche vom Ende.<br/>              |
| <dl> <dt>SC- \_ Suche \_ relativ</dt> </dl>        | Startet die Suche von der aktuellen Position aus.<br/> |



 

</dd> <dt>

*loffset* \[ in\]
</dt> <dd>

Anzahl der Datenobjekte aus dem Verweis Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Um in eine Datei zu lesen oder in diese zu schreiben, geben [**Sie Read**](iscardfileaccess-read.md) bzw. [**Write**](iscardfileaccess-write.md) an.

Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscardfileaccess**](iscardfileaccess.md)
</dt> <dt>

[**Lesen**](iscardfileaccess-read.md)
</dt> <dt>

[**Schreiben**](iscardfileaccess-write.md)
</dt> </dl>

 

 
