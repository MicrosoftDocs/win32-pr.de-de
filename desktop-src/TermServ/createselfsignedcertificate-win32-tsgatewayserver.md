---
title: Die Methode "kreateselfsignedcertificate" der Win32_TSGatewayServer-Klasse
description: Erstellt ein selbst signiertes Zertifikat und gibt den Zertifikat Hash als \ 0034; out \ 0034; zurück. Parame.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "kreateselfsignedcertificate"
- Methode Remotedesktopdienste der Methode "kreateselfsignedcertificate", Win32_TSGatewayServer Klasse
- Win32_TSGatewayServer-Klasse Remotedesktopdienste, Methode "kreateselfsignedcertificate"
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4258566856a5fbc277053b65afe972751855d831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475639"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a>Methode "| ateselfsignedcertificate" der Win32-Klasse "t- \_ Gatewayserver"

Erstellt ein selbst signiertes Zertifikat und gibt den Zertifikat Hash als einen out-Parameter zurück. Außerdem wird der Text "TS- \_ Gateway \_ selbst \_ signiertes \_ Zertifikat" der Zertifikat Kontext Eigenschaft hinzugefügt, sodass das Zertifikat als Remotedesktop Gateway-Zertifikat (RD-Gateway) erkannt wird. Diese Methode verwendet einen RD-Gateway spezifischen Schlüssel Container, um das Zertifikat zu erstellen.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Subjetname* \[ in\]
</dt> <dd>

Der Antragsteller Name des selbst signierten Zertifikats.

</dd> <dt>

*CertHash* \[ vorgenommen\]
</dt> <dd>

Der Zertifikat Hash.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Gatewayserver**](win32-tsgatewayserver.md)
</dt> </dl>

 

