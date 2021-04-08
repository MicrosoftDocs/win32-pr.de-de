---
description: Wenn die transformssecure-Richtlinie auf 1 festgelegt wird, wird dem Installer mitgeteilt, dass Transformationen lokal auf dem Computer des Benutzers an einem Speicherort, an dem der Benutzer keinen Schreibzugriff hat, zwischengespeichert werden sollen.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: Transformssecure-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69180c797008f34755cfa415c7a76fb5f7721f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861903"
---
# <a name="transformssecure-policy"></a>Transformssecure-Richtlinie

Wenn die transformssecure-Richtlinie auf 1 festgelegt wird, wird dem Installer mitgeteilt, dass Transformationen lokal auf dem Computer des Benutzers an einem Speicherort, an dem der Benutzer keinen Schreibzugriff hat, zwischengespeichert werden sollen. Das Festlegen dieser Richtlinie entspricht dem Festlegen der [transformssecure-Eigenschaft](transformssecure.md) , mit dem Unterschied, dass der Bereich anders ist. Das Festlegen der transformssecure-Richtlinie gilt für alle Pakete, die auf einem bestimmten Computer installiert sind. Das Festlegen der transformssecure-Eigenschaft gilt unabhängig vom Computer für das Paket.

Der Zweck dieser Richtlinie besteht darin, einen sicheren Transformations Speicher mit Reisenden Benutzern von Windows 2000 bereitzustellen. Ab Windows Server 2003 ist der Standardwert dieser Richtlinie 1.

Wenn diese Richtlinie festgelegt ist, kann bei einer [Wartungs Installation](maintenance-installation.md) nur die Transformation aus dem gesicherten Cache verwendet werden. Wenn das Installationsprogramm feststellt, dass die Transformation auf dem lokalen Computer fehlt, versucht das Installationsprogramm, die Transformation wiederherzustellen. Damit das Installationsprogramm die Transformation wiederherstellen kann, muss sich die sichere Transformation in der Quell Liste des Installationspakets in einer autorisierten Quelle befinden. Weitere Informationen finden Sie unter [Quellen Resilienz](source-resiliency.md). Die Wartungs Installation schlägt fehl, wenn die Transformation nicht verfügbar ist oder nicht geladen werden kann.

Wenn diese Richtlinie auf Windows Server 2003 nicht festgelegt ist, wird das Standardverhalten verwendet, um die Transformationen an einem sicheren Speicherort zu speichern. Wenn die Richtlinie in allen Versionen vor Windows Server 2003 nicht festgelegt ist, wird das Standardverhalten verwendet, um die Transformationen im Benutzerprofil zu speichern.

Weitere Informationen finden Sie auch unter [gesicherte Transformationen](secured-transforms.md) .

Windows Installer interpretiert die [transformsatsource-Richtlinie](transformsatsource-policy.md) so, dass Sie mit der transformssecure-Richtlinie identisch ist.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



