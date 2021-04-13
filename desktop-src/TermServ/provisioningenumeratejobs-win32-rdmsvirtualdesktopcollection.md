---
title: Provisioningenenumeratejobs-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Listet die Bereitstellungs Aufträge virtueller Desktops für diesen Dienst auf.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Provisioningenumschlag-Methode Remotedesktopdienste
- Provisioningenenumeratejobs-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, provisioningenenumeratejobs-Methode
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
ms.openlocfilehash: aaa2b54a0599c2bbcaf6b0f9a9acb3ab3028389b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518998"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Provisioningenumeratejobs-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse

Listet die Bereitstellungs Aufträge virtueller Desktops für diesen Dienst auf.

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

*JobType* \[ in\]
</dt> <dd>

Eine ganze Zahl, die den Typ des aufzuzählenden Auftrags angibt.

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

*Collectionalias* \[ in\]
</dt> <dd>

Der Alias der aufzuzählenden Auflistung virtueller Desktops. Der Standardwert für diesen Parameter ist false. er gibt an, dass alle ausgeführte Aufträge aufgezählt werden sollen.

</dd> <dt>

*Jobguids* \[ vorgenommen\]
</dt> <dd>

Ein Array, das die **GUIDs** der aufzuzählenden Bereitstellungs Aufträge enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ CIMv2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ rdmsvirtualdesktopcollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





