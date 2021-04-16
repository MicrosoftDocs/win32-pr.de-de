---
description: Ruft das Datenfeld aus der Application Protocol Data Unit (APDU) ab und platziert es in einem Byte Puffer Objekt.
ms.assetid: fbffeeeb-56e5-4484-b294-8b6f59c919eb
title: 'Iscardcmd:: get_data-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: feb6a8c28316bd4fd08160063606d3e15054fd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530221"
---
# <a name="iscardcmdget_data-method"></a>Iscardcmd:: get- \_ Daten Methode

\[Die Methode " **get \_ Data** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die Methode **get \_ Data** Ruft das Datenfeld aus der [*Anwendungsprotokoll Daten-Einheit*](../secgloss/a-gly.md) (APDU) ab und platziert es in einem Byte Puffer Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Data(
  [out] LPBYTEBUFFER *ppData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppData* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das Byte Puffer Objekt (**IStream**), das das APDU-Datenfeld enthält, wenn zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *ppData* -Parameter ist ungültig.<br/>  |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppData* übermittelt.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                        |



 

## <a name="remarks"></a>Bemerkungen

Um das Datenfeld des APDU festzulegen, nennen Sie [**Put \_ Data**](iscardcmd-put-data.md).

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie das Datenfeld der [*Anwendungsprotokoll Daten-Einheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) abgerufen wird. In diesem Beispiel wird davon ausgegangen, dass pibytedata ein gültiger Zeiger auf eine Instanz der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle ist und dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Retrieve the data.
hr = pISCardCmd->get_Data(&pIByteData);
if (FAILED(hr)) 
{
    printf("Failed get_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scarddat. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscardcmd**](iscardcmd.md)
</dt> <dt>

[**\_Daten einfügen**](iscardcmd-put-data.md)
</dt> </dl>

 

 
