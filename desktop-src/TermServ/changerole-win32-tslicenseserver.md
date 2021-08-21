---
title: ChangeRole-Methode der Win32_TSLicenseServer Klasse
description: Ändert den Ermittlungsbereich des Remotedesktop Lizenzservers. Der Ermittlungsbereich bestimmt, Remotedesktop-Sitzungshost (RD-Sitzungshost) Server im Netzwerk den Lizenzserver automatisch entdecken können.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- ChangeRole-Remotedesktopdienste
- ChangeRole-Methode Remotedesktopdienste , Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer klasse Remotedesktopdienste , ChangeRole-Methode
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
ms.openlocfilehash: f010fc1c8d31382040d79bd811e4a472af4269d503d2810e44320717ebbc5e35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575080"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a>ChangeRole-Methode der Win32 \_ TSLicenseServer-Klasse

Ändert den Ermittlungsbereich des Remotedesktop Lizenzservers. Der Ermittlungsbereich bestimmt, Remotedesktop-Sitzungshost (RD-Sitzungshost) Server im Netzwerk den Lizenzserver automatisch entdecken können.

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ServerRole* \[ In\]
</dt> <dd>

Ermittlungsbereich für den Remotedesktop Lizenzserver. Sie können einen der folgenden Werte festlegen.

<dt>

0
</dt> <dd>

RD-Sitzungshost Server in derselben Arbeitsgruppe können den Lizenzserver finden.

</dd> <dt>

1
</dt> <dd>

RD-Sitzungshost Server in derselben Domäne können den Lizenzserver finden. Sie müssen als Domänenadministrator angemeldet sein, um diesen Wert festlegen zu können.

</dd> <dt>

2
</dt> <dd>

RD-Sitzungshost Server aus mehreren Domänen in derselben Gesamtstruktur können den Lizenzserver entdecken. Sie müssen als Unternehmensadministrator angemeldet sein, um diesen Wert festlegen zu können.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

