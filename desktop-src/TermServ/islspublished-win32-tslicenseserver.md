---
title: Islspublished-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob der Remotedesktop Lizenzserver in Active Directory Domain Services (AD \ 160; DS) veröffentlicht wird.
ms.assetid: 0e97c9df-5cb0-4e28-8436-08093a8667d9
ms.tgt_platform: multiple
keywords:
- Islspublished-Methode Remotedesktopdienste
- Islspublished-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, islspublished-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPublished
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69add751497ed52a107ea7183bb4b7cce4ea88c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339979"
---
# <a name="islspublished-method-of-the-win32_tslicenseserver-class"></a>Islspublished-Methode der Win32- \_ Klasse "zlicenseserver"

Ruft ab, ob der Remotedesktop Lizenzserver in Active Directory Domain Services (AD DS) veröffentlicht wird.

## <a name="syntax"></a>Syntax


```mof
uint32 IsLSPublished(
  [out] boolean Published
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Veröffentlicht* \[ vorgenommen\]
</dt> <dd>

Boolescher Wert, der angibt, ob der Lizenzserver in AD DS veröffentlicht wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Wenn der Lizenzserver in AD DS veröffentlicht wird, kann er automatisch durch Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server in derselben Gesamtstruktur erkannt werden.

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

 

