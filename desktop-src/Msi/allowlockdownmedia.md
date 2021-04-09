---
description: Wenn Sie den Wert dieser pro-Computer-System Richtlinie auf &\# 0034; 1&\# 0034; festlegen, können nicht Administratoren verwaltete Anwendungen von auf Medien gespeicherten Quellen, z. b. einer CD-ROM, installieren.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869604"
---
# <a name="allowlockdownmedia"></a>AllowLockdownMedia

Wenn Sie den Wert dieser pro-Computer- [System Richtlinie](system-policy.md) auf "1" festlegen, können nicht Administratoren [*verwaltete Anwendungen*](m-gly.md) von auf Medien gespeicherten Quellen, z. b. einer CD-ROM, installieren. Siehe [quellresilienz](source-resiliency.md). Wenn diese Richtlinie beispielsweise festgelegt ist, kann ein Benutzer, der nicht Administrator ist, eine Medienquelle verwenden, um zugewiesene oder veröffentlichte Anwendungen oder Anwendungen zu installieren, die für alle Benutzer installiert werden. Wenn Sie diese Richtlinie festlegen, können Benutzer, die nicht Administratoren sind, auch bei einer erweiterten Installation Programme mit LocalSystem-Berechtigungen ausführen.

Der Standardwert dieser Richtlinie ist 1 nur auf Computern, auf denen Windows Vista ausgeführt wird und die keiner Domäne hinzugefügt werden. Die Standardeinstellung auf anderen Computern besteht darin, dass nicht-Administratoren verwaltete Anwendungen nicht über eine Quelle installieren können, die sich auf dem Medium befindet.

Da diese Richtlinie Benutzern, die kein Administrator sind, die Installation mit Berechtigungen ermöglicht, die Sie nicht standardmäßig haben, bevor Sie diese Richtlinie festlegen, sollten Sie berücksichtigen, ob Sie ein geeignetes Maß an Sicherheit für den Benutzer bereitstellt. Die Standardeinstellung wird empfohlen, um eine sichere Umgebung sicherzustellen.

Weitere Informationen zum Sichern von Installationen und zum Verwenden digitaler Zertifikate finden Sie unter [Richtlinien zum Erstellen sicherer Installationen](guidelines-for-authoring-secure-installations.md) und [digitaler Signaturen und Windows Installer](digital-signatures-and-windows-installer.md) und [Herunterladen einer-Installation aus dem Internet](downloading-an-installation-from-the-internet.md).

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Durch Festlegen dieser Richtlinie können nicht Administratoren beliebige Programme unter "LocalSystem"-Berechtigungen ausführen, wenn Sie über ein Windows Installer Paket verfügen, mit dem diese Programme installiert oder gestartet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellen Resilienz](source-resiliency.md)
</dt> <dt>

[AllowLockdownBrowse](allowlockdownbrowse.md)
</dt> </dl>

 

 



