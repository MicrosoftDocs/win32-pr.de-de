---
title: Getprovisioningproperties-Methode der Win32_RDMSCollectionProperties-Klasse
description: Ruft die Bereitstellungs Eigenschaften der Sammlung virtueller Desktops ab.
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- Getprovisioningproperties-Methode Remotedesktopdienste
- Getprovisioningproperties-Methode Remotedesktopdienste, Win32_RDMSCollectionProperties-Klasse
- Win32_RDMSCollectionProperties-Klasse Remotedesktopdienste, getprovisioningproperties-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ca58f82d2918441e5da3cf53d442497c1a6a2eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337529"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a>Getprovisioningproperties-Methode der Win32- \_ Klasse rdmscollectionproperties

Ruft die Bereitstellungs Eigenschaften der Sammlung virtueller Desktops ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Poolvhdtype* \[ vorgenommen\]
</dt> <dd>

Gibt das VHD-Format (virtuelle Festplatte) des virtuellen Computerpools in der Sammlung an.

<dt>

Klon
</dt> <dd>

Eine geklonte VHD.

</dd> <dt>

Diffdisk
</dt> <dd>

Eine differenzierende VHD.

</dd> </dl> </dd> <dt>

*Mastervmlocation* \[ vorgenommen\]
</dt> <dd>

Empfängt den Pfad zum Master-VM-Image.

</dd> <dt>

*NamePrefix* \[ vorgenommen\]
</dt> <dd>

Empfängt das namens Präfix, das am Anfang der Namen virtueller Computer angefügt werden soll.

</dd> <dt>

*Namestartindex* \[ vorgenommen\]
</dt> <dd>

Start Index.

</dd> <dt>

*Localvmlocation* \[ vorgenommen\]
</dt> <dd>

Empfängt den lokalen Pfad zu den virtuellen Maschinen auf den Hyper-V-Servern. Wenn dieser Parameter auf **null** festgelegt ist oder leer ist, wird das Standardverzeichnis der virtuellen Maschine verwendet.

</dd> <dt>

*Localgoldvmlocation* \[ vorgenommen\]
</dt> <dd>

Empfängt den lokalen Pfad zum Golden VHD-Abbild, wenn der *poolvhdtpe* -Parameter auf "diffdisk" festgelegt ist. Wenn dieser Parameter auf **null** festgelegt ist oder leer ist, wird das Standardverzeichnis der virtuellen Maschine verwendet.

</dd> <dt>

*Runfromsmb* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Wert, der angibt, ob die Auflistung von einer SMB-Freigabe (Server Message Block) ausgeführt werden soll. " **True** ", um die virtuellen Computer über eine SBM-Freigabe auszuführen. sonst **False**.

</dd> <dt>

*Smblozierung* \[ vorgenommen\]
</dt> <dd>

Empfängt den Pfad zur SMB-Freigabe, wenn die SMB-Freigabe aktiviert ist.

</dd> <dt>

*Smbstreaming* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Wert, der angibt, ob SMB-Streaming aktiviert ist. **True** , wenn die SMB-Freigabe aktiviert ist. sonst **False**.

</dd> <dt>

*Vmdomain* \[ vorgenommen\]
</dt> <dd>

Empfängt den Domänen Namen der virtuellen Computer in der Sammlung.

</dd> <dt>

*Vmou* \[ vorgenommen\]
</dt> <dd>

Empfängt die Active Directory Organisationseinheit (OU) der virtuellen Computer in der Sammlung.

</dd> <dt>

*ProductKey* \[ vorgenommen\]
</dt> <dd>

Empfängt die Betriebssystem-Product Keys für die virtuellen Computer in der Sammlung.

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

[**Win32- \_ rdmscollectionproperties**](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





