---
title: Provisioningjobexecute-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Führt einen Bereitstellungs Auftrag für virtuelle Desktops aus.
ms.assetid: 69f0cc6a-7eef-4cd9-94ac-f0c7e52d02d8
ms.tgt_platform: multiple
keywords:
- Provisioningjobexecute-Methode Remotedesktopdienste
- Provisioningjobexecute-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, provisioningjobexecute-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobExecute
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c632a6bdc5fc5c4a128941d8a6c8b4379ddf9629
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478870"
---
# <a name="provisioningjobexecute-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Provisioningjobexecute-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse

Führt einen Bereitstellungs Auftrag für virtuelle Desktops aus.

## <a name="syntax"></a>Syntax


```mof
uint32 ProvisioningJobExecute(
  [in]  string JobInputXml,
  [out] string JobGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Jobinputxml* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die die Bereitstellungs Informationen im XML-Format enthält.

</dd> <dt>

*Jobguid* \[ vorgenommen\]
</dt> <dd>

Die **GUID** , die den zu testender Bereitstellungs Auftrag eindeutig identifiziert.

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

 

 





