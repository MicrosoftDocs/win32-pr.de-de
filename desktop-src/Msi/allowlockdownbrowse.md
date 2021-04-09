---
description: Das Festlegen des Werts für diese Computer spezifische System Richtlinie auf &\# 0034; 1&\# 0034; ermöglicht nicht Administratoren die Verwendung eines Dialog Felds zum Durchsuchen, um nach Quellen verwalteter Anwendungen zu suchen.
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864499"
---
# <a name="allowlockdownbrowse"></a>AllowLockdownBrowse

Wenn Sie den Wert dieser pro-Computer- [System Richtlinie](system-policy.md) auf "1" festlegen, können nicht Administratoren mit einem Dialog Feld " [Durchsuchen](browse-dialog.md) " nach Quellen [*verwalteter Anwendungen*](m-gly.md)suchen. Quellen können Medien wie z. b. CD-ROM, URLs und Netzwerk Orte enthalten. Weitere Informationen finden Sie unter [Quellen Resilienz](source-resiliency.md). Der Standardwert für Windows Installer ist, dass nicht-Administratoren nach neuen Quellen verwalteter Anwendungen suchen können. Die einzigen verfügbaren Quellen sind die, die bereits in der Quell Liste des Produkts registriert sind. Wenn diese Richtlinie festgelegt ist, kann ein Benutzer, der nicht Administrator ist, nach neuen Quellen für zugewiesene oder veröffentlichte Anwendungen oder Anwendungen suchen, die für alle Benutzer installiert werden. Durch das Festlegen von AllowLockdownBrowse können auch nicht Administratoren Programme bei einer erweiterten Installation unter "LocalSystem"-Berechtigungen ausführen.

Die Standardeinstellung wird empfohlen, um eine sichere Umgebung sicherzustellen.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Durch Festlegen dieser Richtlinie können nicht Administratoren beliebige Programme unter "LocalSystem"-Berechtigungen ausführen, wenn Sie über ein Windows Installer Paket verfügen, mit dem diese Programme installiert oder gestartet werden.

[Disablebrowse](disablebrowse.md) überschreibt AllowLockdownBrowse und verhindert das Durchsuchen, auch wenn AllowLockdownBrowse festgelegt ist.

Informationen zur Interaktion dieser Richtlinie mit Installations Quellen finden Sie unter [Verwalten von Installations Quellen](managing-installation-sources.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellen Resilienz](source-resiliency.md)
</dt> <dt>

[AllowLockdownMedia](allowlockdownmedia.md)
</dt> </dl>

 

 



