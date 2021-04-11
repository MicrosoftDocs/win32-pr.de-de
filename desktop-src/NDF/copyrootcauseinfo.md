---
title: Copyrootkauseinfo-Funktion (ndattributils. h)
description: Erstellt eine Kopie einer rootkauseingabe FO-Struktur.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- Copyrootkausin FO-Funktion NDF
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5093d7af6458668a763aa206cacd22a0526aa521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949660"
---
# <a name="copyrootcauseinfo-function"></a>Copyrootkausin FO-Funktion

Die **copyrootcauseingefo** -Funktion erstellt eine Kopie einer [**rootkauseingabe FO**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) -Struktur.

## <a name="syntax"></a>Syntax


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dest* \[ vorgenommen\]
</dt> <dd>

Typ: **[**rootkauseinfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

Die zu Aktualisier Ende-Struktur.

</dd> <dt>

_Source * \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **Konstanten [**rootkauseinfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

Die vorhandene zu kopierende-Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Mögliche Rückgabewerte sind u. a. die folgenden.



| Rückgabecode                                                                                   | Beschreibung                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich ausgeführt.<br/>                                         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Mindestens ein Parameter wurde nicht ordnungsgemäß bereitgestellt.<br/>          |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um diesen Vorgang abzuschließen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rootkauseingefo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





