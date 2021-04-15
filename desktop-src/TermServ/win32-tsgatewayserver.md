---
title: Win32_TSGatewayServer-Klasse
description: Wird für Server spezifische Vorgänge Remotedesktop Gateway (RD-Gateway) verwendet.
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServer-Klasse Remotedesktopdienste
- Win32_TSGatewayServer Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: b7dee009521c59b606010be085fcb0447558898d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476383"
---
# <a name="win32_tsgatewayserver-class"></a>Win32-Klasse "- \_ Gatewayserver"

Wird für Server spezifische Vorgänge Remotedesktop Gateway (RD-Gateway) verwendet.

## <a name="syntax"></a>Syntax

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ zgatewayserver** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ zgatewayserver** " verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreateselfsignedcertificate"**](createselfsignedcertificate-win32-tsgatewayserver.md) | Erstellt ein selbst signiertes Zertifikat mit einem angegebenen Antragsteller Namen und gibt den Zertifikat Hash als einen out-Parameter zurück.<br/> |
| [**Exportieren**](export-win32-tsgatewayserver.md)                                           | Gibt die RD-Gateway Server-Konfiguration als XML-Zeichenfolge zurück.<br/>                                                       |
| [**Importieren**](import-win32-tsgatewayserver.md)                                           | Importiert eine angegebene Konfiguration auf den RD-Gateway Server.<br/>                                                             |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



 

