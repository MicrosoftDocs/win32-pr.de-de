---
title: CreateSelfSignedCertificate-Methode der Win32_TSGatewayServer-Klasse
description: Erstellt ein selbstsignes Zertifikat und gibt den Zertifikathash als \ 0034;out \ 0034; zurück. Parameter.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- CreateSelfSignedCertificate-Methode Remotedesktopdienste
- CreateSelfSignedCertificate-Methode Remotedesktopdienste , Win32_TSGatewayServer-Klasse
- Win32_TSGatewayServer Klasse Remotedesktopdienste , CreateSelfSignedCertificate-Methode
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
ms.openlocfilehash: 200b08da8d5eea9f31405a357650384081c407df4eb76820cd47a111e6b66aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139053"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a>CreateSelfSignedCertificate-Methode der Win32 \_ TSGatewayServer-Klasse

Erstellt ein selbstsigniertes Zertifikat und gibt den Zertifikathash als "out"-Parameter zurück. Außerdem fügt der \_ Zertifikatkontexteigenschaft den Text "TS GATEWAY \_ SELF \_ SIGNED \_ CERTIFICATE" hinzu, sodass das Zertifikat als Remotedesktop Gatewayzertifikat (RD-Gateway) erkannt wird. Diese Methode verwendet einen RD-Gateway-spezifischen Schlüsselcontainer, um das Zertifikat zu erstellen.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SubjectName* \[ In\]
</dt> <dd>

Antragstellername des selbstsignieren Zertifikats.

</dd> <dt>

*CertHash* \[ out\]
</dt> <dd>

Der Zertifikathash.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayServer**](win32-tsgatewayserver.md)
</dt> </dl>

 

