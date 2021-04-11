---
title: Deactivateserverautomatic-Methode der Win32_TSLicenseServer-Klasse
description: Deaktiviert den Remotedesktop Lizenzserver über das Internet.
ms.assetid: 6e049d7f-1753-484d-98b8-fde66d16b5ab
ms.tgt_platform: multiple
keywords:
- Deactivateserverautomatic-Methode Remotedesktopdienste
- Deactivateserverautomatic-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, deactivateserverautomatic-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d466b5f7814d6004bafdd01bce161a481eacf26a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040270"
---
# <a name="deactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a>Deactivateserverautomatic-Methode der Win32- \_ Klasse "zlicenseserver"

Deaktiviert den Remotedesktop Lizenzserver über das Internet.

## <a name="syntax"></a>Syntax


```mof
uint32 DeactivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Activationstatus* \[ vorgenommen\]
</dt> <dd>

Der zurückgegebene Aktivierungs Status kann einer der folgenden sein.

<dt>

0
</dt> <dd>

Der Remotedesktop Lizenzserver wird aktiviert.

</dd> <dt>

1
</dt> <dd>

Der Remotedesktop Lizenzserver ist nicht aktiviert.

</dd> <dt>

2
</dt> <dd>

Es ist ein unbekannter Fehler aufgetreten. Es ist nicht bekannt, ob der Remotedesktop Lizenzserver aktiviert ist.

</dd> </dl> </dd> </dl>

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

 

