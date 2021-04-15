---
title: Deletereport-Methode der Win32_TSLicenseReport-Klasse
description: Löscht ein Berichts Objekt auf dem Remotedesktop-Lizenzserver. Dabei handelt es sich nicht um eine statische Methode.
ms.assetid: cc70526c-7ce5-4d55-b72e-8a5e8799b1d8
ms.tgt_platform: multiple
keywords:
- Deletereport-Methode Remotedesktopdienste
- Deletereport-Methode Remotedesktopdienste, Win32_TSLicenseReport-Klasse
- Win32_TSLicenseReport-Klasse Remotedesktopdienste, deletereport-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.DeleteReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a96c8626e4ecc1f89d0f2fcefa69845fec4df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517450"
---
# <a name="deletereport-method-of-the-win32_tslicensereport-class"></a>Deletereport-Methode der Win32- \_ Klasse "zlicensereport"

Löscht ein Berichts Objekt auf dem Remotedesktop-Lizenzserver. Dabei handelt es sich nicht um eine statische Methode.

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteReport();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Dabei handelt es sich nicht um eine statische Methode. Diese Methode muss von einem Bericht Objekt pro Benutzer-Lizenz Verwendung aufgerufen werden.

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

[**Win32-Datei- \_ /licensereport**](win32-tslicensereport.md)
</dt> </dl>

 

