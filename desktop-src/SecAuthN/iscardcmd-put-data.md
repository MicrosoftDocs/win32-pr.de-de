---
description: Legt das Datenfeld in der Application Protocol Data Unit (APDU) fest.
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: Iscardcmd::p ut_Data-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 58c1fa7d709eff1ed0618f52a83825f5110c4457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130260"
---
# <a name="iscardcmdput_data-method"></a>Iscardcmd::p UT- \_ Daten Methode

\[Die **Put \_ Data** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Put \_ Data** -Methode legt das Datenfeld in der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ in\]
</dt> <dd>

Ein Zeiger auf das Byte Puffer Objekt (**IStream**), das in das APDU-Datenfeld kopiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>    |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *pData* -Parameter ist ungültig.<br/>  |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *pData* übergeben.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                       |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen neuen Datenteil der Nachricht festlegen, wird die Länge des Daten Felds berechnet und im P3-Parameter von APDU gespeichert. Rufen [**Sie get \_ P3**](iscardcmd-get-p3.md)auf, um die Länge des Daten Felds abzurufen.

Rufen [**Sie get \_ Data**](iscardcmd-get-data.md)auf, um das Datenfeld aus dem APDU abzurufen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie das Datenfeld in der [*Anwendungsprotokoll Dateneinheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) festgelegt wird. In diesem Beispiel wird davon ausgegangen, dass pibytedata ein gültiger Zeiger auf eine Instanz der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle ist und dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
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

[**\_Daten erhalten**](iscardcmd-get-data.md)
</dt> <dt>

[**\_P3 erhalten**](iscardcmd-get-p3.md)
</dt> <dt>

[**Iscardcmd**](iscardcmd.md)
</dt> </dl>

 

 
