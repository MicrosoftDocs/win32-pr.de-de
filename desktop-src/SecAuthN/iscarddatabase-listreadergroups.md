---
description: Die listreadergroups-Methode ruft die Namen der Lesergruppen ab, die in der Smartcard-Datenbank registriert sind.
ms.assetid: 81f6356a-92eb-4d27-abfe-e4a32de14d1c
title: 'Iscarddatabase:: listreadergroups-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaderGroups
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 00753b0ca3964dc5a35e26db0eec2aedda4d2511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129325"
---
# <a name="iscarddatabaselistreadergroups-method"></a>Iscarddatabase:: listreadergroups-Methode

\[Die **listreadergroups** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **listreadergroups** -Methode ruft die Namen der [*Lesergruppen*](../secgloss/r-gly.md) ab, die in der Smartcard-Datenbank registriert sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT ListReaderGroups(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaderGroups
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LocaleID* \[ in\]
</dt> <dd>

Sprach Lokalisierungs-ID.

</dd> <dt>

*ppreadergroups* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein SafeArray von bstrinray, das die Namen der smartcardlesegruppen enthält, die die Suchparameter bei erfolgreicher Ausführung erfüllt haben. **Null** , wenn der Vorgang fehlgeschlagen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>             |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                            |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in " *ppreadergroups*" übergeben.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                |



 

## <a name="remarks"></a>Bemerkungen

Rufen Sie zum Abrufen aller bekannten [*Smartcards*](../secgloss/s-gly.md) oder [*Leser*](../secgloss/r-gly.md) [**listcards**](iscarddatabase-listcards.md) bzw. [**listreaders**](iscarddatabase-listreaders.md) auf.

Zum Abrufen des [*primären Dienstanbieters*](../secgloss/p-gly.md) oder der Schnittstellen einer bestimmten Karte [**getprovidercardid**](iscarddatabase-getprovidercardid.md) bzw. [**listcardinterfaces**](iscarddatabase-listcardinterfaces.md) .

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscarddatabase**](iscarddatabase.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie die Namen der in der Smartcard-Datenbank registrierten Lesergruppen abrufen.


```C++
LPSAFEARRAY pGroups = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaderGroups(0x0409,  // English (US)
                                    &pGroups);
if (FAILED(hr))
{
   printf("Failed ListReaderGroups\n");
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

[**Listcards**](iscarddatabase-listcards.md)
</dt> <dt>

[**Listreaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
