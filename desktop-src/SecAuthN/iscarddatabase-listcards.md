---
description: Die listcards-Methode ruft alle smartcardnamen ab, die den angegebenen Schnittstellen Bezeichnerzeichen (GUIDs), der angegebenen ATR-Zeichenfolge oder beiden entsprechen.
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: 'Iscarddatabase:: List Cards-Methode (scardmgr. h)'
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
ms.openlocfilehash: e8a5bf56aa27a044d29e2e0153698bfefe69e1d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751681"
---
# <a name="iscarddatabaselistcards-method"></a>Iscarddatabase:: listcards-Methode

\[Die **listcards** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **listcards** -Methode ruft alle smartcardnamen ab, die den angegebenen Schnittstellen Bezeichnerzeichen (GUIDs), der angegebenen [*ATR-Zeichenfolge*](../secgloss/a-gly.md)oder beiden entsprechen.

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

*Patr* \[ in\]
</dt> <dd>

Zeiger auf eine [*Smartcard*](../secgloss/s-gly.md) -ATR-Zeichenfolge. Die ATR-Zeichenfolge muss in einen [**ibytebuffer**](ibytebuffer.md)gepackt werden.

</dd> <dt>

*pinterfaceguids* \[ in\]
</dt> <dd>

Zeiger auf ein SafeArray von COM-Schnittstellen Bezeichners (GUIDs) im BSTR-Format.

</dd> <dt>

*LocaleID* \[ in\]
</dt> <dd>

Der Bezeichner der Sprachlokalisierung.

</dd> <dt>

*ppcardnames* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein SafeArray von bstrinray, das die Namen der Smartcards enthält, die die Suchparameter bei erfolgreicher Ausführung erfüllt haben. **Null** , wenn der Vorgang fehlgeschlagen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Es wurde ein fehlerhafter Zeiger übermittelt.<br/>      |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Um [*alle bekannten Reader*](../secgloss/r-gly.md) oder [*Reader*](../secgloss/r-gly.md)abzurufen, rufen Sie [**listreaders**](iscarddatabase-listreaders.md) bzw. [**listreadergroups**](iscarddatabase-listreadergroups.md) auf.

Zum Abrufen des [*primären Dienstanbieter*](../secgloss/p-gly.md) oder der Schnittstellen einer bestimmten Karte [**getprovidercardid**](iscarddatabase-getprovidercardid.md) bzw. [**listcardinterfaces**](iscarddatabase-listcardinterfaces.md) .

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscarddatabase**](iscarddatabase.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie die smartcardnamen abgerufen werden, die der angegebenen ATR-Zeichenfolge entsprechen.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardmgr. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscarddatabase ist als 1461aac8-6810-11D0-918f -00aa00c18068 definiert.<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getprovidercardid**](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[**Iscarddatabase**](iscarddatabase.md)
</dt> <dt>

[**Listcardinterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**Listreadergroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**Listreaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
