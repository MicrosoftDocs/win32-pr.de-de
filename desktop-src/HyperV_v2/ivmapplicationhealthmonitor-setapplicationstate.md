---
description: Legt den Integritäts Status einer Anwendung fest, die auf einem virtuellen Computer ausgeführt wird.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: 'Ivmapplicationhealthmonitor:: stapplicationstate-Methode'
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
ms.openlocfilehash: 8e6c64ecec827f6f75f382fbca7aadf8fc0c7dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348511"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a>Ivmapplicationhealthmonitor:: stapplicationstate-Methode

Legt den Integritäts Status einer Anwendung fest, die auf einem virtuellen Computer ausgeführt wird.

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

Eine **BSTR** -Darstellung der **GUID** , die die Anwendung identifiziert. Es liegt in der Verantwortung der aufrufenden Anwendung, die Bezeichner zu erstellen und zu verwalten, die für die überwachten Anwendungen verwendet werden.

</dd> <dt>

*Name* \[ in\]
</dt> <dd>

Der Anzeigename der Anwendung. Dieser Name wird in einem Informations Ereignis-Protokolleintrag für die Zustandsänderung verwendet.

</dd> <dt>

*Status* \[ in\]
</dt> <dd>

Ein Wert der Enumeration des [**Anwendungs \_ Zustands**](application-state.md) , der den neuen Integritäts Status der Anwendung angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Der Status der Anwendungen, die auf dem virtuellen Computer ausgeführt werden, wird im Eigenschafts Wert **OperationalStatus** \[ 1 \] der [**MSVM-Klasse \_ heartbeatcomponent**](msvm-heartbeatcomponent.md) widergespiegelt.

Um dieses Programmier Element zu verwenden, müssen die Windows 8-Integrations Komponenten auf dem virtuellen Computer installiert sein, auf dem die Anwendung ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                      |
| Version<br/>                  | Integrations Komponenten für Windows 8<br/>                                                           |
| IDL<br/>                      | <dl> <dt>Vmapplicationhealthmonitor. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmapplicationhealthmonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




