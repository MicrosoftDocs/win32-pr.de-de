---
description: Die GetProviderCardId-Methode ruft den Bezeichner (GUID) des primären Dienstanbieters für die angegebene Smartcard ab.
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: ISCardDatabase::GetProviderCardId-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.GetProviderCardId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 814eec89f8ff92d81dd911101d79e516500f0baeb363dd4148bd466de849bc24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577280"
---
# <a name="iscarddatabasegetprovidercardid-method"></a>ISCardDatabase::GetProviderCardId-Methode

\[Die **GetProviderCardId-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **GetProviderCardId-Methode** ruft den Bezeichner (GUID) des [*primären Dienstanbieters*](../secgloss/p-gly.md) für die angegebene [*Smartcard*](../secgloss/s-gly.md)ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrCardName* \[ In\]
</dt> <dd>

Name der Smartcard.

</dd> <dt>

*ppguidProviderId* \[ out\]
</dt> <dd>

Zeiger auf den Bezeichner des primären Dienstanbieters (GUID), falls erfolgreich; **NULL,** wenn der Vorgang fehlgeschlagen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                              |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein ungültiger Zeiger wurde in *ppguidProviderId* übergeben.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                  |



 

## <a name="remarks"></a>Hinweise

Um die Schnittstellen der Smartcard aufzulisten, rufen [**Sie ListCardInterfaces auf.**](iscarddatabase-listcardinterfaces.md)

Um alle bekannten [*Smartcards*](../secgloss/s-gly.md)abzurufen, rufen [*Leser*](../secgloss/r-gly.md) und [*Lesergruppen*](../secgloss/r-gly.md) [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)bzw. [**ListReaderGroups**](iscarddatabase-listreadergroups.md) auf.

Eine Liste aller methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardDatabase.**](iscarddatabase.md)

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Abrufen des Bezeichners des primären Dienstanbieters für die angegebene Smartcard.


```C++
BSTR     bstrCard = NULL;
LPGUID   pguidProvId = NULL;
HRESULT  hr;

bstrCard = SysAllocString(L"My Card");
hr = pISCDataBase->GetProviderCardId(bstrCard,&pguidProvId);
if (FAILED(hr))
{
   printf("Failed GetProviderCardId\n");
}
else
{
    // Use pguidProvId as needed.
}

// Free BSTR when done.
if ( NULL != bstrCard )
{
    SysFreeString(bstrCard);
    bstrCard=NULL;
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISCardDatabase**](iscarddatabase.md)
</dt> <dt>

[**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
