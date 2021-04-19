---
description: Wenn die transformssecure-Eigenschaft auf 1 festgelegt wird, wird dem Installer mitgeteilt, dass Transformationen lokal auf dem Computer des Benutzers an einem Speicherort zwischengespeichert werden, an dem der Benutzer keinen Schreibzugriff hat.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: Transformssecure (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b7a30ab5e94fb646e2e8960b60fd97dc35557c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369266"
---
# <a name="transformssecure-property"></a>Transformssecure (Eigenschaft)

Wenn die **transformssecure** -Eigenschaft auf 1 festgelegt wird, wird dem Installer mitgeteilt, dass Transformationen lokal auf dem Computer des Benutzers an einem Speicherort zwischengespeichert werden, an dem der Benutzer keinen Schreibzugriff hat. Das Festlegen dieser Eigenschaft entspricht dem Festlegen der [transformssecure-Richtlinie](transformssecure-policy.md) , mit der Ausnahme, dass der Bereich anders ist. Das Festlegen der transformssecure-Richtlinie gilt für alle Pakete, die von einem bestimmten Benutzer installiert wurden. Das Festlegen der **transformssecure** -Eigenschaft gilt unabhängig vom Benutzer für das Paket.

Der Zweck dieser Eigenschaft ist die Bereitstellung von sicherem Transformations Speicher mit Reisenden Benutzern von Windows 2000. Wenn diese Eigenschaft festgelegt ist, kann bei einer [Wartungs Installation](maintenance-installation.md) nur die Transformation aus dem angegebenen Pfad verwendet werden. Wenn der Pfad nicht verfügbar ist, tritt bei der Wartungs Installation ein Fehler auf. Eine Quelle für jede sichere Transformation muss sich daher am Speicherort der Quelle des Installationspakets befinden. Wenn das Installationsprogramm feststellt, dass die Transformation auf dem lokalen Computer fehlt, kann die Transformation aus dieser Quelle wieder hergestellt werden.

## <a name="remarks"></a>Bemerkungen

Windows Installer interpretiert die [**transformsatsource**](transformsatsource.md) -Eigenschaft so, dass Sie mit der **transformssecure** -Eigenschaft identisch ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Daten Bank Transformationen](database-transforms.md)
</dt> </dl>

 

 




