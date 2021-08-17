---
description: Die GetResponse-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der APDU-Befehle (oder einen Teil eines APDU-Befehls) überträgt, die andernfalls nicht von den verfügbaren Protokollen übertragen werden konnten.
ms.assetid: 1aa83d38-d46d-4d3b-8f57-0256e5875e35
title: ISCardISO7816::GetResponse-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetResponse
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 21646b7de844509b28bb0ea437fa76cd9fa835932333677f919872daecb3ce60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481148"
---
# <a name="iscardiso7816getresponse-method"></a>ISCardISO7816::GetResponse-Methode

\[Die **GetResponse-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **GetResponse-Methode** erstellt einen APDU-Befehl [*(Application Protocol Data Unit),*](../secgloss/a-gly.md) der APDU-Befehle (oder einen Teil eines APDU-Befehls) überträgt, die andernfalls nicht von den verfügbaren Protokollen übertragen werden konnten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResponse(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lDataLength,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byP1* \[ In\]
</dt> <dd>

Gemäß ISO 7816-4 sollte P1 null (RFU) sein.

</dd> <dt>

*byP2* \[ In\]
</dt> <dd>

Gemäß ISO 7816-4 sollte P2 null (RFU) sein.

</dd> <dt>

*lDataLength* \[ In\]
</dt> <dd>

Länge der übertragenen Daten.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**ISCardCmd-Schnittstellenobjekt**](iscardcmd.md) oder **NULL.**

Bei der Rückgabe wird er mit dem APDU-Befehl gefüllt, der von diesem Vorgang erstellt wurde. Wenn *ppCmd* auf **NULL** festgelegt wurde, wird intern ein [**ISCardCmd-Smartcardobjekt**](iscardcmd.md) erstellt und über den *ppCmd-Zeiger* zurückgegeben. [](../secgloss/s-gly.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein ungültiger Zeiger wurde übergeben.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardISO7816**](iscardiso7816.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 ist als 53B6AA68-3F56-11D0-916B-00AA00C18068 definiert.<br/>        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
