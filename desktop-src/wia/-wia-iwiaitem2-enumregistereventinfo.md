---
description: 'Die IWiaItem2:: enumregistereventinfo-Methode erstellt einen Enumerator, mit dem Sie Informationen zu Ereignissen abrufen können, für die eine Anwendung registriert ist.'
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'IWiaItem2:: enumregistereventinfo-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129428"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a>IWiaItem2:: enumregistereventinfo-Methode

Die **IWiaItem2:: enumregistereventinfo** -Methode erstellt einen Enumerator, mit dem Sie Informationen zu Ereignissen abrufen können, für die eine Anwendung registriert ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Nicht verwendet. Auf 0 festlegen.

</dd> <dt>

" *Peer-GUID* \[ " in\]
</dt> <dd>

Geben Sie Folgendes ein: * Konstante *GUID \** _

Ein Zeiger auf einen Bezeichner, der das Hardware Ereignis angibt, für das Sie Registrierungsinformationen abrufen möchten.

</dd> <dt>

_ppIEnum * \[ out\]
</dt> <dd>

Typ: **[ **ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Die Adresse eines Zeigers auf die [**ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung ruft diese Methode auf, um ein Enumeratorobjekt für die Ereignis Informationen zu erstellen. **IWiaItem2:: enumregistereventinfo** speichert die Adresse der [**ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) -Schnittstelle des Enumeratorobjekts im *ppienum* -Parameter. Das Programm verwendet dann den Schnittstellen Zeiger, um die Eigenschaften des Ereignisses aufzulisten, für das es registriert ist.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppienum* -Parameter empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
