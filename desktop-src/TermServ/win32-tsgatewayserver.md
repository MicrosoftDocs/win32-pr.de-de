---
title: Win32_TSGatewayServer-Klasse
description: Wird für serverspezifische vorgänge Remotedesktop Gateway (RD Gateway) verwendet.
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServer-Klasse Remotedesktopdienste
- Win32_TSGatewayServer-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cd6c24447e7ba3bc22788484b2ac9e437ee947243c17a676728d2a336bd326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603887"
---
# <a name="win32_tsgatewayserver-class"></a>Win32 \_ TSGatewayServer-Klasse

Wird für serverspezifische vorgänge Remotedesktop Gateway (RD Gateway) verwendet.

## <a name="syntax"></a>Syntax

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSGatewayServer-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSGatewayServer-Klasse** verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**CreateSelfSignedCertificate**](createselfsignedcertificate-win32-tsgatewayserver.md) | Erstellt ein selbstsigniertes Zertifikat mit einem angegebenen Antragstellernamen und gibt den Zertifikathash als "out"-Parameter zurück.<br/> |
| [**Exportieren**](export-win32-tsgatewayserver.md)                                           | Gibt die RD-Gatewayserverkonfiguration als XML-Zeichenfolge zurück.<br/>                                                       |
| [**Importieren**](import-win32-tsgatewayserver.md)                                           | Importiert eine bestimmte Konfiguration auf den RD-Gatewayserver.<br/>                                                             |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



 

