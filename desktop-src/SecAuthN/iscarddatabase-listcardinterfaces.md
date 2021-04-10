---
description: Die listcardinterfaces-Methode ruft die Bezeichner (GUIDs) aller Schnittstellen ab, die für die angegebene Smartcard unterstützt werden.
ms.assetid: c9dfd17e-f4a9-47d3-974e-66e78bc4b06a
title: 'Iscarddatabase:: listcardinterfaces-Methode (scardmgr. h)'
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
ms.openlocfilehash: d52324edd4a502388ac6064de07a6ab58a68074d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214406"
---
# <a name="iscarddatabaselistcardinterfaces-method"></a>Iscarddatabase:: listcardinterfaces-Methode

\[Die **listcardinterfaces** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **listcardinterfaces** -Methode ruft die Bezeichner (GUIDs) aller Schnittstellen ab, die für die angegebene [*Smartcard*](../secgloss/s-gly.md)unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT ListCardInterfaces(
  [in]  BSTR        bstrCardName,
  [out] LPSAFEARRAY *ppInterfaceGuids
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrincardname* \[ in\]
</dt> <dd>

Der Name der Smartcard.

</dd> <dt>

*ppinterfaceguids* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die Schnittstellen-GUIDs, wenn erfolgreich; **Null** , wenn der Vorgang fehlgeschlagen ist

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>               |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                              |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppinterfaceguids* übermittelt.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                  |



 

## <a name="remarks"></a>Bemerkungen

Rufen Sie [**getprovidercardid**](iscarddatabase-getprovidercardid.md)auf, um den [*primären Dienstanbieter*](../secgloss/p-gly.md) der Smartcard abzurufen.

Rufen Sie zum Abrufen aller bekannten [*Smartcards*](../secgloss/s-gly.md), [*Leser*](../secgloss/r-gly.md)und [*Lesergruppen*](../secgloss/r-gly.md) [**listcards**](iscarddatabase-listcards.md), [**listreaders**](iscarddatabase-listreaders.md)und [**listreadergroups**](iscarddatabase-listreadergroups.md) auf.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscarddatabase**](iscarddatabase.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

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

[**Listcards**](iscarddatabase-listcards.md)
</dt> <dt>

[**Listreadergroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**Listreaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
