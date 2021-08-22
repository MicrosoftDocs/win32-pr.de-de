---
description: Durch Festlegen der Richtlinie TransformsSecure auf 1 wird das Installationsprogramm darüber informiert, dass Transformationen lokal auf dem Computer des Benutzers an einem Speicherort zwischengespeichert werden sollen, an dem der Benutzer keinen Schreibzugriff hat.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: TransformationenSichere Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6300a25db8e80003ff2a03afd56b168b9697f92764f16a26e99860c0a27796bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500295"
---
# <a name="transformssecure-policy"></a>TransformationenSichere Richtlinie

Durch Festlegen der Richtlinie TransformsSecure auf 1 wird das Installationsprogramm darüber informiert, dass Transformationen lokal auf dem Computer des Benutzers an einem Speicherort zwischengespeichert werden sollen, an dem der Benutzer keinen Schreibzugriff hat. Das Festlegen dieser Richtlinie ist identisch mit dem Festlegen der [TRANSFORMSSECURE-Eigenschaft,](transformssecure.md) außer dass der Bereich anders ist. Das Festlegen von TransformationenSicherte Richtlinie gilt für alle Pakete, die auf einem bestimmten Computer installiert sind. Das Festlegen der TRANSFORMSSECURE-Eigenschaft gilt unabhängig vom Computer für das Paket.

Der Zweck dieser Richtlinie besteht in der Bereitstellung einer sicheren Transformationsspeicherung mit unterwegs Windows 2000. Ab Windows Server 2003 ist der Standardwert dieser Richtlinie 1.

Wenn diese Richtlinie festgelegt ist, kann eine [Wartungsinstallation](maintenance-installation.md) nur die Transformation aus dem gesicherten Cache verwenden. Wenn das Installationsprogramm ermittelt, dass die Transformation auf dem lokalen Computer fehlt, versucht das Installationsprogramm, die Transformation wiederherzustellen. Damit das Installationsprogramm die Transformation wiederherstellen kann, muss sich die sichere Transformation an einer autorisierten Quelle in der Quellliste des Installationspakets befinden. Weitere Informationen finden Sie unter [Quellresilienz.](source-resiliency.md) Die Wartungsinstallation schlägt fehl, wenn die Transformation nicht verfügbar ist oder nicht geladen werden kann.

Wenn Windows Server 2003 nicht festgelegt ist, ist das Standardverhalten, die Transformationen an einem sicheren Ort zu speichern. Bei allen Versionen vor Windows Server 2003 besteht das Standardverhalten im Speichern der Transformationen im Benutzerprofil, wenn die Richtlinie nicht festgelegt ist.

Weitere Informationen [finden Sie unter Sichere Transformationen.](secured-transforms.md)

Windows Das Installationsprogramm interpretiert die [TransformsAtSource-Richtlinie](transformsatsource-policy.md) so, dass sie mit der TransformsSecure-Richtlinie identisch ist.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_** \\ **MACHINE-Softwarerichtlinien** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



