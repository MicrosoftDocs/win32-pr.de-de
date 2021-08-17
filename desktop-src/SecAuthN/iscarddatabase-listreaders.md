---
description: Die ListReaders-Methode ruft die Namen der Smartcardleser ab, die in der Smartcard-Datenbank registriert sind.
ms.assetid: e1ca85a1-9206-4c09-ba0f-10b60e472dfb
title: ISCardDatabase::ListReaders-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaders
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c7ae9c41a8b1894ec0c233c6090f8ab990e275e95bc20c4768171fe867412838
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141133"
---
# <a name="iscarddatabaselistreaders-method"></a>ISCardDatabase::ListReaders-Methode

\[Die **ListReaders-Methode** ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ListReaders-Methode** ruft die Namen [](../secgloss/r-gly.md) der Smartcardleser ab, die in der [*Smartcard-Datenbank registriert sind.*](../secgloss/s-gly.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT ListReaders(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaders
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*localeId* \[ In\]
</dt> <dd>

Sprachlokalisierungs-ID.

</dd> <dt>

*ppReaders* \[ out\]
</dt> <dd>

Zeiger auf ein SAFEARRAY von BSTRs, das bei Erfolg die Namen der Smartcardleser enthält; **NULL,** wenn der Vorgang fehlgeschlagen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                       |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppReaders übergeben.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                           |



 

## <a name="remarks"></a>Hinweise

Um alle bekannten [*Smartcards oder*](../secgloss/s-gly.md) Readergruppen [*abzurufen,*](../secgloss/r-gly.md)rufen [**Sie ListCards bzw.**](iscarddatabase-listcards.md) [**ListReaderGroups**](iscarddatabase-listreadergroups.md) auf.

So rufen Sie [*den primären Dienstanbieter oder*](../secgloss/p-gly.md) die Schnittstellen einer bestimmten Karte [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) bzw. [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) ab.

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardDatabase**](iscarddatabase.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Abrufen der Namen der Smartcardleser, die in der Smartcard-Datenbank registriert sind.


```C++
LPSAFEARRAY pReaders = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaders(0x0409,  // English (US)
                               &pReaders);
if (FAILED(hr))
{
   printf("Failed ListReaders\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardDatabase ist als 1461AAC8-6810-11D0-918F-00AA00C18068 definiert.<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetProviderCardId**](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[**ISCardDatabase**](iscarddatabase.md)
</dt> <dt>

[**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> </dl>

 

 
