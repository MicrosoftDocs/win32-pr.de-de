---
title: Issecureaccessallowed-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob ein Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Remotedesktopdienste Client Zugriffs Lizenzen anfordern darf (RDS \ 160; CALs) auf dem Remotedesktop-Lizenzserver.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- Issecureaccessallowed-Methode Remotedesktopdienste
- Issecureaccessallowed-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, issecureaccessallowed-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsSecureAccessAllowed
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf35fd8b38139027955fde51a209000435744f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517741"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a>Issecureaccessallowed-Methode der Win32- \_ Klasse "zlicenseserver"

Ruft ab, ob ein Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Remotedesktopdienste Client Zugriffs Lizenzen (RDS-CALs) vom Remotedesktop Lizenzserver anfordern darf.

## <a name="syntax"></a>Syntax


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*zname* \[ in\]
</dt> <dd>

Der Name des RD-Sitzungshost Servers.

</dd> <dt>

*Zulässig* \[ vorgenommen\]
</dt> <dd>

Boolescher Wert, der angibt, ob der RD-Sitzungshost Server RDS-CALs vom Lizenzserver anfordern darf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Der zurückgegebene Wert basiert auf der Gruppenrichtlinien Einstellung "Lizenzserver-Sicherheitsgruppe" und der lokalen Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenzserver.

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
</dt> <dt>

[**Islssecgrpgpabled**](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 

