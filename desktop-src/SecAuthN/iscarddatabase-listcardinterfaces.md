---
description: Die ListCardInterfaces-Methode ruft die Bezeichner (GUIDs) aller Schnittstellen ab, die für die angegebene Smartcard unterstützt werden.
ms.assetid: c9dfd17e-f4a9-47d3-974e-66e78bc4b06a
title: ISCardDatabase::ListCardInterfaces-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCardInterfaces
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b97569f967c76c985eb05099a21ed10e90456563a871f3e5d9803c6a5875ebdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008108"
---
# <a name="iscarddatabaselistcardinterfaces-method"></a>ISCardDatabase::ListCardInterfaces-Methode

\[Die **ListCardInterfaces-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ListCardInterfaces-Methode** ruft die Bezeichner (GUIDs) aller Schnittstellen ab, die für die angegebene [*Smartcard unterstützt werden.*](../secgloss/s-gly.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT ListCardInterfaces(
  [in]  BSTR        bstrCardName,
  [out] LPSAFEARRAY *ppInterfaceGuids
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrCardName* \[ In\]
</dt> <dd>

Name der Smartcard.

</dd> <dt>

*ppInterfaceGuids* \[ out\]
</dt> <dd>

Zeiger auf die Schnittstellen-GUIDs, falls erfolgreich; **NULL,** wenn der Vorgang fehlgeschlagen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                              |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppInterfaceGuids übergeben.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                  |



 

## <a name="remarks"></a>Hinweise

Rufen Sie [**getProviderCardId**](iscarddatabase-getprovidercardid.md) [*auf,*](../secgloss/p-gly.md) um den primären Dienstanbieter der Smartcard abzurufen.

Zum Abrufen aller bekannten [*Smartcards*](../secgloss/s-gly.md) [*rufen*](../secgloss/r-gly.md)Leser und Lesergruppen [**ListCards,**](iscarddatabase-listcards.md) [**ListReaders**](iscarddatabase-listreaders.md)und [**ListReaderGroups**](iscarddatabase-listreadergroups.md) auf. [](../secgloss/r-gly.md)

Eine Liste aller von dieser Schnittstelle bereitgestellten Methoden finden Sie unter [**ISCardDatabase**](iscarddatabase.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcard-Fehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Abrufen der Bezeichner der Schnittstellen, die für die angegebene Smartcard unterstützt werden.


```C++
BSTR         bstrCard = NULL;
LPSAFEARRAY  pGuids = NULL;
HRESULT      hr;

bstrCard = SysAllocString(L"GemSAFE");
// Call the function for the specified card.
hr = pISCDataBase->ListCardInterfaces(bstrCard,
                                      &pGuids);
if (FAILED(hr))
{
   printf("Failed ListCardInterfaces\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
   // Free BSTR when done.
   if (bstrCard)
       SysFreeString(bstrCard);
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

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
