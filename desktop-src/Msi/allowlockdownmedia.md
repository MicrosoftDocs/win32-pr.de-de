---
description: Wenn Sie den Wert dieser Computersystemrichtlinie auf &\# 0034;1&0034; festlegen, können benutzer ohne Administratorrolle verwaltete Anwendungen aus Quellen installieren, die auf Medien gespeichert sind, z. B. \# cd-ROM.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8e280fbd4941c43221d2178811fe341d4f963657bc4e6e5c9e8a19ec31acf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821860"
---
# <a name="allowlockdownmedia"></a>AllowLockdownMedia

Wenn Sie den Wert [](system-policy.md) dieser computerspezifischen Systemrichtlinie auf "1" festlegen, [](m-gly.md) können Benutzer ohne Administratorrolle verwaltete Anwendungen aus Quellen installieren, die auf Medien gespeichert sind, z. B. cd-ROM. Weitere Informationen [finden Sie unter Quellresilienz.](source-resiliency.md) Wenn diese Richtlinie beispielsweise festgelegt ist, kann ein nichtadministrativer Benutzer eine Medienquelle verwenden, um zugewiesene oder veröffentlichte Anwendungen oder Anwendungen zu installieren, die für alle Benutzer installiert werden. Durch festlegen dieser Richtlinie können Benutzer ohne Administratorrechte während einer Installation mit erhöhten Rechten auch Programme mit LocalSystem-Berechtigungen ausführen.

Der Standardwert dieser Richtlinie ist 1 nur auf Computern, auf denen Windows Vista ausgeführt wird und die nicht einer Domäne beigetreten sind. Die Standardeinstellung auf anderen Computern ist, dass benutzer, die keine Administratoren sind, verwaltete Anwendungen nicht aus einer Quelle installieren können, die sich auf Medien befindet.

Da diese Richtlinie Benutzern, die kein Administrator sind, die Installation mit Berechtigungen ermöglicht, über die sie standardmäßig nicht verfügen, sollten Sie vor dem Festlegen dieser Richtlinie überlegen, ob sie eine angemessene Sicherheitsstufe für Ihren Benutzer bietet. Die Standardeinstellung wird empfohlen, um eine sichere Umgebung sicherzustellen.

Weitere Informationen zum Sichern von Installationen und zum Verwenden digitaler Zertifikate finden Sie unter [Richtlinien](guidelines-for-authoring-secure-installations.md) für die Erstellung sicherer Installationen und digitaler Signaturen und [Windows Installer](digital-signatures-and-windows-installer.md) und Herunterladen einer Installation aus [dem Internet.](downloading-an-installation-from-the-internet.md)

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_** \\ **MACHINE-Softwarerichtlinien** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Hinweise

Durch festlegen dieser Richtlinie können Benutzer ohne Administratorrechte auch beliebige Programme mit LocalSystem-Berechtigungen ausführen, wenn sie über ein Windows Installer-Paket verfügen, das diese Programme installiert oder startet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellresilienz](source-resiliency.md)
</dt> <dt>

[AllowLockdownBrowse](allowlockdownbrowse.md)
</dt> </dl>

 

 



