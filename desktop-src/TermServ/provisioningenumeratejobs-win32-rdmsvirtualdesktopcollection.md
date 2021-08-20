---
title: ProvisioningEnumerateJobs-Methode der Win32_RDMSVirtualDesktopCollection Klasse
description: Aufzählen von Bereitstellungsaufträgen für virtuelle Desktops für diesen Dienst.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- ProvisioningEnumerateJobs-Remotedesktopdienste
- ProvisioningEnumerateJobs-Methode Remotedesktopdienste , Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection klasse Remotedesktopdienste , ProvisioningEnumerateJobs-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b24ef80acdb29c75327447f61db7dae1689a883f69c9e19ef199710de216fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118350222"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>ProvisioningEnumerateJobs-Methode der Win32 \_ RDMSVirtualDesktopCollection-Klasse

Aufzählen von Bereitstellungsaufträgen für virtuelle Desktops für diesen Dienst.

## <a name="syntax"></a>Syntax


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*JobType* \[ In\]
</dt> <dd>

Eine ganze Zahl, die den Typ des aufzählenden Auftrags angibt.

Dieser Parameter kann auf einen der folgenden Werte festgelegt werden:

<dt>

0
</dt> <dd>

Ausführen von Aufträgen

</dd> <dt>

1
</dt> <dd>

Abgeschlossene Aufträge

</dd> </dl> </dd> <dt>

*CollectionAlias* \[ In\]
</dt> <dd>

Der Alias der auflistung virtueller Desktops, die aufzählt werden soll. Der Standardwert für diesen Parameter ist FALSE, der angibt, dass alle ausgeführten Aufträge aufzählt werden sollen.

</dd> <dt>

*JobGuids* \[ out\]
</dt> <dd>

Ein Array, das die **GUIDs der** aufzählenden Bereitstellungsaufträge enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2-Rdms \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





