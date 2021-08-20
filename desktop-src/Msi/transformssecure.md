---
description: Durch Festlegen der TRANSFORMSSECURE-Eigenschaft auf 1 wird das Installationsprogramm darüber informiert, dass Transformationen lokal auf dem Computer des Benutzers an einem Speicherort zwischengespeichert werden sollen, an dem der Benutzer keinen Schreibzugriff hat.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: TRANSFORMSSECURE-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af3432b8f895d4d9f5d0fe643ef8106e01e28ad64fb2db177e968fbc13d88de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141633"
---
# <a name="transformssecure-property"></a>TRANSFORMSSECURE-Eigenschaft

Durch Festlegen der **TRANSFORMSSECURE-Eigenschaft** auf 1 wird das Installationsprogramm darüber informiert, dass Transformationen lokal auf dem Computer des Benutzers an einem Speicherort zwischengespeichert werden sollen, an dem der Benutzer keinen Schreibzugriff hat. Das Festlegen dieser Eigenschaft entspricht dem Festlegen der [Richtlinie TransformsSecure,](transformssecure-policy.md) mit der Ausnahme, dass der Bereich unterschiedlich ist. Das Festlegen der TransformsSecure-Richtlinie gilt für alle Pakete, die von einem bestimmten Benutzer installiert werden. Das Festlegen der **TRANSFORMSSECURE-Eigenschaft** gilt für das Paket, unabhängig vom Benutzer.

Der Zweck dieser Eigenschaft ist die Bereitstellung eines sicheren Transformierungsspeichers für reisende Benutzer von Windows 2000. Wenn diese Eigenschaft festgelegt ist, kann eine [Wartungsinstallation](maintenance-installation.md) nur die Transformation aus dem angegebenen Pfad verwenden. Wenn der Pfad nicht verfügbar ist, schlägt die Installation der Wartung fehl. Daher muss sich eine Quelle für jede sichere Transformation am Speicherort der Quelle des Installationspakets befinden. Wenn das Installationsprogramm dann feststellt, dass die Transformation auf dem lokalen Computer fehlt, kann es die Transformation aus dieser Quelle wiederherstellen.

## <a name="remarks"></a>Hinweise

Windows Das Installationsprogramm interpretiert die [**TRANSFORMSATSOURCE-Eigenschaft**](transformsatsource.md) so, dass sie mit der **TRANSFORMSSECURE-Eigenschaft** identisch ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Datenbanktransformationen](database-transforms.md)
</dt> </dl>

 

 




