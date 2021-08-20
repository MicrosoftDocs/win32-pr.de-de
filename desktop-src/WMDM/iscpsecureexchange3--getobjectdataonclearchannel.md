---
title: GetObjectDataOnClearChannel-Methode
description: Die GetObjectDataOnClearChannel-Methode überträgt einen Block von Objektdaten auf einem clear-Kanal zurück an Windows Media Geräte-Manager.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- GetObjectDataOnClearChannel-Methode windows Media Geräte-Manager
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c10e09697653c2ef1235ae9a3ea3a93a45437d1cf45a1f4de72ec99b0812b9b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619870"
---
# <a name="getobjectdataonclearchannel-method"></a>GetObjectDataOnClearChannel-Methode

Die **GetObjectDataOnClearChannel-Methode** überträgt einen Block von Objektdaten auf einem clear-Kanal zurück an Windows Media Geräte-Manager.

Diese Methode ist mit [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) identisch, mit der Ausnahme, dass die von dieser Methode zurückgegebenen Daten nicht verschlüsselt sind. Folglich ist diese Methode effizienter.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* 
</dt> <dd>

Zeiger auf das Geräteobjekt.

</dd> <dt>

*Pdata* 
</dt> <dd>

Zeiger auf einen Puffer zum Empfangen von Daten.

</dd> <dt>

*pdwSize* 
</dt> <dd>

Zeiger auf ein **DWORD** mit der Übertragungsgröße.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn die Methode fehlschlägt, wird ein **HRESULT-Fehlercode** zurückgegeben.



| Rückgabecode                                                                                                | Beschreibung                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**WMDM \_ E \_ MAC \_ CHECK \_ FAILED**</dt> </dl> | Der Nachrichtenauthentifizierungscode ist ungültig.<br/>                                    |
| <dl> <dt>**WMDM \_ E \_ NORIGHTS**</dt> </dl>           | Der Aufrufer verfügt nicht über die erforderlichen Rechte zum Ausführen des angeforderten Vorgangs.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Fehler bei der Methode. Beenden Sie die Interaktion mit dem Inhaltsanbieter.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Ein Parameter ist ein ungültiger oder **NULL-Zeiger.**<br/>                                   |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                     | Es ist ein unbekannter Fehler aufgetreten.<br/>                                                   |



 

## <a name="remarks"></a>Hinweise

Zum Übertragen von Daten ruft Windows Media Geräte-Manager die [TransferContainerDataOnClearChannel-Methode](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) auf, um die Containerdaten abzurufen. **GetObjectDataOnClearChannel** wird dann aufgerufen, um Objektdatenblöcke vom Inhaltsanbieter an Windows Media Geräte-Manager zu übertragen. Wenn S \_ OK zurückgegeben wird und *pdwSize* auf 0 (null) festgelegt ist, fordert Windows Media Geräte-Manager keine weiteren Daten an.

Diese Methode ist mit [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) identisch, mit der Ausnahme, dass die von dieser Methode zurückgegebenen Daten nicht verschlüsselt sind. Folglich ist diese Methode effizienter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>WMSCP.idl</dt> </dl>    |
| Bibliothek<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[**ISCPSecureExchange3-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





