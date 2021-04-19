---
description: Wenn Sie den Wert dieser pro-Computer-System Richtlinie auf &\# 0034; 1&0034 festlegen, \# wird verhindert, dass nicht Administratoren mithilfe eines Dialog Felds zum Durchsuchen nach Quellen verwalteter Anwendungen suchen, die auf Medien wie CD-ROM gespeichert sind.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: Disablebrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342824"
---
# <a name="disablebrowse"></a>Disablebrowse

Wenn Sie den Wert dieser pro-Computer- [System Richtlinie](system-policy.md) auf "1" festlegen, wird verhindert, dass nicht Administratoren mithilfe eines Dialog Felds zum [Durchsuchen](browse-dialog.md) nach Quellen [*verwalteter Anwendungen*](m-gly.md) suchen, die auf Medien wie CD-ROM gespeichert sind. Das Kombinations Feld "Funktion von: verwenden" für die direkte Eingabe ist gesperrt, und das "Durchsuchen..." die Schaltfläche ist deaktiviert. Weitere Informationen zum Durchsuchen von Quellen finden Sie unter [Quellen Resilienz](source-resiliency.md).

Disablebrowse überschreibt AllowLockdownBrowse und verhindert das Durchsuchen, auch wenn AllowLockdownBrowse festgelegt ist.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Bemerkungen

In einigen Fällen, in denen "disablebrowse" festgelegt ist, kann ein nicht administrativer Benutzer weiterhin verwaltete Anwendungen aus Quellen auf ordnungsgemäß gekennzeichneten Medien installieren. Durch das Festlegen der disablebrowse-Richtlinie wird nur die Funktion zum Durchsuchen der Quellen deaktiviert. Sie kann verwendet werden, um zu verhindern, dass ein Benutzer, der nicht Administrator ist, während einer Installation auf Abruf, Neuinstallation oder Reparatur eine neue Quelle durchsucht. Wenn [AllowLockdownMedia](allowlockdownmedia.md) festgelegt ist, kann der nicht administrative Benutzer dennoch eine verwaltete Anwendung von einem ordnungsgemäß gekennzeichneten Medium installieren.

Disablebrowse hindert den nicht Administrator daran, zu einem neuen Medien Speicherort oder einem anderen Quell Speicherort zu navigieren. Ausführliche Informationen zum Sichern von Medienquellen verwalteter Anwendungen finden Sie unter [Resilienz der Quelle](source-resiliency.md).

Informationen zur Interaktion dieser Richtlinie mit Installations Quellen finden Sie unter [Verwalten von Installations Quellen](managing-installation-sources.md).

 

 



