---
description: Die ListCards-Methode ruft alle Smartcardnamen ab, die mit den angegebenen Schnittstellenbezeichnern (GUIDs), der angegebenen ATR-Zeichenfolge oder beiden übereinstimmen.
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: ISCardDatabase::ListCards-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c34d5d1449b2ef8f34fa87d3a70ecf37787d423a0d5df71ecd15e5f722d112ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014530"
---
# <a name="iscarddatabaselistcards-method"></a>ISCardDatabase::ListCards-Methode

\[Die **ListCards-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ListCards-Methode** ruft alle Smartcardnamen ab, die mit den angegebenen Schnittstellenbezeichnern (GUIDs), der angegebenen [*ATR-Zeichenfolge*](../secgloss/a-gly.md)oder beiden übereinstimmen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAtr* \[ In\]
</dt> <dd>

Zeiger auf eine [*SMARTCARD-ATR-Zeichenfolge.*](../secgloss/s-gly.md) Die ATR-Zeichenfolge muss in einen [**IByteBuffer**](ibytebuffer.md)gepackt werden.

</dd> <dt>

*pInterfaceGuids* \[ In\]
</dt> <dd>

Zeiger auf ein SAFEARRAY von COM-Schnittstellenbezeichnern (GUIDs) im BSTR-Format.

</dd> <dt>

*localeId* \[ In\]
</dt> <dd>

Sprachenlokalisierungsbezeichner.

</dd> <dt>

*ppCardNames* \[ out\]
</dt> <dd>

Zeiger auf ein SAFEARRAY von BSTRs, das die Namen der Smartcards enthält, die bei Erfolg die Suchparameter erfüllt haben; **NULL,** wenn der Vorgang fehlgeschlagen ist.

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

Um alle bekannten [*Reader*](../secgloss/r-gly.md) oder [*Leser*](../secgloss/r-gly.md)abzurufen, rufen [**Sie ListReaders**](iscarddatabase-listreaders.md) bzw. [**ListReaderGroups**](iscarddatabase-listreadergroups.md) auf.

So rufen Sie den [*primären Dienst*](../secgloss/p-gly.md) oder die Schnittstellen einer bestimmten Karte [**ab: GetProviderCardId**](iscarddatabase-getprovidercardid.md) bzw. [**ListCardInterfaces.**](iscarddatabase-listcardinterfaces.md)

Eine Liste aller methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardDatabase.**](iscarddatabase.md)

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Abrufen der Smartcardnamen, die mit der angegebenen ATR-Zeichenfolge übereinstimmen.


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
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

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
