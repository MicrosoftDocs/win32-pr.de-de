---
title: Islsinzlsgroup-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob der Remotedesktop Lizenzserver Mitglied der Remotedesktop-Lizenzserver Gruppe auf einem Domänen Controller in einer bestimmten Domäne ist.
ms.assetid: a6ad7f09-8972-47d4-8b3b-cd129b400ea8
ms.tgt_platform: multiple
keywords:
- Islsinzlsgroup-Methode Remotedesktopdienste
- Islsinzlsgroup-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, islsinzlsgroup-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSinTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3577e4632167612b4d71841501a2a2845203a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338350"
---
# <a name="islsintslsgroup-method-of-the-win32_tslicenseserver-class"></a>Islsinzlsgroup-Methode der Win32- \_ Klasse "zlicenseserver"

Ruft ab, ob der Remotedesktop Lizenzserver Mitglied der Remotedesktop-Lizenzserver Gruppe auf einem Domänen Controller in einer bestimmten Domäne ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsLSinTSLSGroup(
  [in]  string  Domain,
  [out] boolean IsMember
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Domäne* \[ in\]
</dt> <dd>

Der Domänenname.

</dd> <dt>

*IsMember* \[ vorgenommen\]
</dt> <dd>

Boolescher Wert, der angibt, ob der Lizenzserver Mitglied der Remotedesktop-Lizenzserver Gruppe in der Domäne ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Wenn kein Domänen Name angegeben ist, wird ein Domänen Controller in derselben Domäne wie der Lizenzserver abgefragt.

Der Lizenzserver sollte Mitglied der Gruppe Remotedesktop-Lizenzserver sein, wenn der Server für die Verwendung des Domänen-oder Gesamtstruktur-Ermittlungs Bereichs konfiguriert ist. Wenn der Lizenzserver nicht Mitglied dieser Gruppe ist, funktionieren die pro-Benutzer-Lizenz Nachverfolgung und-Berichterstellung nicht.

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

[**Addlstozlsgroup**](addlstotslsgroup-win32-tslicenseserver.md)
</dt> <dt>

[**Removelsfromzlsgroup**](removelsfromtslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

