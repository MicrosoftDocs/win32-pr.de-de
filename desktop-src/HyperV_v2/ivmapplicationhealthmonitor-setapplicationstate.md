---
description: Legt den Integritätsstatus einer Anwendung fest, die auf einem virtuellen Computer ausgeführt wird.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: IVmApplicationHealthMonitor::SetApplicationState-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 785b5e6254bde84497f4fcf72d15b20ff16ccd7319ecc3631c0864b3e4992655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392355"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a>IVmApplicationHealthMonitor::SetApplicationState-Methode

Legt den Integritätsstatus einer Anwendung fest, die auf einem virtuellen Computer ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Eine **BSTR-Darstellung** der **GUID,** die die Anwendung identifiziert. Es liegt in der Verantwortung der aufrufenden Anwendung, die Bezeichner zu erstellen und zu verwalten, die sie für die überwachten Anwendungen verwendet.

</dd> <dt>

*Name* \[ In\]
</dt> <dd>

Der Anzeigename der Anwendung. Dieser Name wird in einem Informationsereignisprotokolleintrag für die Zustandsänderung verwendet.

</dd> <dt>

*Status* \[ In\]
</dt> <dd>

Ein Wert der [**APPLICATION \_ STATE-Enumeration,**](application-state.md) der den neuen Integritätszustand der Anwendung angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Der Status der auf dem virtuellen Computer ausgeführten Anwendungen wird im **OperationalStatus** 1-Eigenschaftswert der \[ \] [**Msvm \_ HeartbeatComponent-Klasse widergespiegelt.**](msvm-heartbeatcomponent.md)

Um dieses Programmierelement verwenden zu können, müssen Windows 8 Integrationskomponenten auf dem virtuellen Computer installiert sein, auf dem die Anwendung ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                      |
| Version<br/>                  | Integrationskomponenten für Windows 8<br/>                                                           |
| Idl<br/>                      | <dl> <dt>VmApplicationHealthMonitor.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




