---
description: Die getprovidercardid-Methode ruft den Bezeichner (GUID) des primären Dienstanbieters für die angegebene Smartcard ab.
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: 'Iscarddatabase:: getprovidercardid-Methode (scardmgr. h)'
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
ms.openlocfilehash: 9f361e83431fa7c6e0a0c2c0ea363bef7e487738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758826"
---
# <a name="iscarddatabasegetprovidercardid-method"></a>Iscarddatabase:: getprovidercardid-Methode

\[Die **getprovidercardid** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **getprovidercardid** -Methode ruft den Bezeichner (GUID) des [*primären Dienstanbieters*](../secgloss/p-gly.md) für die angegebene [*Smartcard*](../secgloss/s-gly.md)ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrincardname* \[ in\]
</dt> <dd>

Der Name der Smartcard.

</dd> <dt>

*ppguidproviderid* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den Bezeichner des primären Dienstanbieters (GUID), wenn erfolgreich; **Null** , wenn der Vorgang fehlgeschlagen ist

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>               |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                              |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppguidproviderid* übermittelt.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                  |



 

## <a name="remarks"></a>Bemerkungen

Um die Schnittstellen der Smartcard aufzulisten, müssen Sie [**listcardinterfaces**](iscarddatabase-listcardinterfaces.md)aufzurufen.

Rufen Sie zum Abrufen aller bekannten [*Smartcards*](../secgloss/s-gly.md), [*Leser*](../secgloss/r-gly.md) und [*Lesergruppen*](../secgloss/r-gly.md) [**listcards**](iscarddatabase-listcards.md), [**listreaders**](iscarddatabase-listreaders.md)und [**listreadergroups**](iscarddatabase-listreadergroups.md) auf.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscarddatabase**](iscarddatabase.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie der Bezeichner des primären Dienstanbieters für die angegebene Smartcard abgerufen wird.


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

[**Iscarddatabase**](iscarddatabase.md)
</dt> <dt>

[**Listcardinterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**Listcards**](iscarddatabase-listcards.md)
</dt> <dt>

[**Listreadergroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**Listreaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
