---
title: Istsintscgroup-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob ein Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Mitglied der lokalen Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenzserver ist.
ms.assetid: 61c39928-3a2b-4a36-ae4e-b9597a12d5e7
ms.tgt_platform: multiple
keywords:
- Istsintscgroup-Methode Remotedesktopdienste
- Istsintscgroup-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, istsintscgroup-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSinTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d666457f053c8fd48abd904d099bfbfa93a0de6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518830"
---
# <a name="istsintscgroup-method-of-the-win32_tslicenseserver-class"></a>Istsintscgroup-Methode der Win32- \_ Klasse "zlicenseserver"

Ruft ab, ob ein Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Mitglied der lokalen Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenzserver ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsTSinTSCGroup(
  [in]  string  tsname,
  [out] boolean IsMember
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*zname* \[ in\]
</dt> <dd>

Der Name des RD-Sitzungshost Servers.

</dd> <dt>

*IsMember* \[ vorgenommen\]
</dt> <dd>

Boolescher Wert, der angibt, ob der RD-Sitzungshost Server Mitglied der lokalen Gruppe "Terminal Server Computer" ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Tltaumiprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Lizenznehmer**](win32-tslicenseserver.md)
</dt> </dl>

 

