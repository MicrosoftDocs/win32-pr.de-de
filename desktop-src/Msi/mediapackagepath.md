---
description: 'Wenn sich der Installationspaketversand mit einer Anwendung nicht im Stammverzeichnis der CD-ROM befindet, die Kunden erhalten, muss die MEDIAPACKAGEPATH-Eigenschaft in der Befehlszeile auf den relativen Pfad der Anwendung auf der CD-ROM festgelegt werden. Wenn der Pfad zum Paket auf dem Medium beispielsweise E: \\ MyPath \\My.msi lautet, verwenden Sie MEDIAPACKAGEPATH=&\# 0034; \\ MyPath \\ & \# 0034;. Administratoren können CD-ROMs von einem Administratorinstallationspunkt aus erstellen. Wenn der Speicherort des Stamms der Installation auf den neuen CD-ROMs geändert wird, muss die MEDIAPACKAGEPATH-Eigenschaft auf den neuen Pfad für die Installation von diesem Medium festgelegt werden. Eine Quelle mit einem Speicherort auf der CD-ROM, der sich von dem im Paket angegebenen unterscheidet, kann nicht verwendet werden. Es ist jedoch nicht erforderlich, diese Eigenschaft zu verwenden, wenn Sie einen Administratorinstallationspunkt aus dem Versandmedium erstellen.'
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: MEDIAPACKAGEPATH-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140afc253e27b3c861f941e88b55f84ad49f43984fcc3a5aaf82d06fe414e6a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926880"
---
# <a name="mediapackagepath-property"></a>MEDIAPACKAGEPATH-Eigenschaft

Wenn sich der Installationspaketversand mit einer Anwendung nicht im Stammverzeichnis der CD-ROM befindet, die Kunden erhalten, muss die **MEDIAPACKAGEPATH-Eigenschaft** in der Befehlszeile auf den relativen Pfad der Anwendung auf der CD-ROM festgelegt werden.

Wenn der Pfad zum Paket auf dem Medium beispielsweise E: \\ MyPath \\My.msi lautet, verwenden Sie MEDIAPACKAGEPATH=" \\ MyPath \\ ".

Administratoren können CD-ROMs von einem Administratorinstallationspunkt aus erstellen. Wenn der Speicherort des Stamms der Installation auf den neuen CD-ROMs geändert wird, muss die **MEDIAPACKAGEPATH-Eigenschaft** auf den neuen Pfad für die Installation von diesem Medium festgelegt werden. Eine Quelle mit einem Speicherort auf der CD-ROM, der sich von dem im Paket angegebenen unterscheidet, kann nicht verwendet werden. Es ist jedoch nicht erforderlich, diese Eigenschaft zu verwenden, wenn Sie einen Administratorinstallationspunkt aus dem Versandmedium erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




