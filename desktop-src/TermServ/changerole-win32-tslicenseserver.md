---
title: Changerole-Methode der Win32_TSLicenseServer-Klasse
description: Ändert den Ermittlungs Bereich des Remotedesktop Lizenzservers. Der Ermittlungs Bereich bestimmt, welche Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server im Netzwerk den Lizenzserver automatisch ermitteln können.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- Changerole-Methode Remotedesktopdienste
- Changerole-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, changerole-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475795"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a>Changerole-Methode der Win32- \_ Klasse "zlicenseserver"

Ändert den Ermittlungs Bereich des Remotedesktop Lizenzservers. Der Ermittlungs Bereich bestimmt, welche Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server im Netzwerk den Lizenzserver automatisch ermitteln können.

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ServerRole* \[ in\]
</dt> <dd>

Ermittlungs Bereich für den Remotedesktop-Lizenzserver. Sie können einen der folgenden Werte festlegen:

<dt>

0
</dt> <dd>

RD-Sitzungshost Server in derselben Arbeitsgruppe können den Lizenzserver ermitteln.

</dd> <dt>

1
</dt> <dd>

RD-Sitzungshost Server in derselben Domäne können den Lizenzserver ermitteln. Sie müssen als Domänen Administrator angemeldet sein, um diesen Wert festzulegen.

</dd> <dt>

2
</dt> <dd>

RD-Sitzungshost Server aus mehreren Domänen in derselben Gesamtstruktur können den Lizenzserver ermitteln. Sie müssen als Unternehmens Administrator angemeldet sein, um diesen Wert festzulegen.

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

 

