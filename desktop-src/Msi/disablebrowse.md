---
description: Durch Festlegen des Werts dieser Systemrichtlinie pro Computer auf &\# 0034;1&\# 0034; wird verhindert, dass nicht administrative Benutzer ein Dialogfeld zum Durchsuchen verwenden, um quellen von verwalteten Anwendungen zu suchen, die auf Medien wie CD-ROM gespeichert sind.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e565cca833d8d771b5bc28dea4483049868995a06acc9a42116611a1df6ce098
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745570"
---
# <a name="disablebrowse"></a>DisableBrowse

Wenn Sie den Wert dieser [Systemrichtlinie](system-policy.md) pro Computer auf "1" festlegen, wird verhindert, dass nicht administrative Benutzer ein [Dialogfeld](browse-dialog.md) zum Durchsuchen verwenden, um quellen von [*verwalteten Anwendungen*](m-gly.md) zu suchen, die auf Medien wie CD-ROM gespeichert sind. Das Kombinationsfeld "Feature verwenden von:" für direkte Eingaben ist gesperrt, und "Durchsuchen..." -Schaltfläche ist deaktiviert. Weitere Informationen zum Durchsuchen von Quellen finden Sie unter [Quellresilienz.](source-resiliency.md)

DisableBrowse überschreibt AllowLockdownBrowse und verhindert das Durchsuchen, auch wenn AllowLockdownBrowse festgelegt ist.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Hinweise

In einigen Fällen, in denen DisableBrowse festgelegt ist, kann ein nicht administrativer Benutzer verwaltete Anwendungen aus Quellen auf ordnungsgemäß bezeichneten Medien installieren. Wenn Sie die Richtlinie DisableBrowse festlegen, wird nur die Funktion zum Navigieren zu Quellen deaktiviert. Sie kann verwendet werden, um zu verhindern, dass ein nicht administrativer Benutzer während einer installation-on-demand-Installation, -Neuinstallation oder -Reparatur zu einer neuen Quelle navigieren kann. Wenn [AllowLockdownMedia](allowlockdownmedia.md) festgelegt ist, kann der nicht administrative Benutzer weiterhin eine verwaltete Anwendung von ordnungsgemäß bezeichneten Medien installieren.

DisableBrowse verhindert, dass der nicht administrative Benutzer zu einem neuen Medienspeicherort oder einem anderen Quellspeicherort navigieren kann. Ausführliche Informationen zum Sichern von Medienquellen verwalteter Anwendungen finden Sie unter [Quellresilienz.](source-resiliency.md)

Informationen zur Interaktion dieser Richtlinie mit Installationsquellen finden Sie unter [Verwalten von Installationsquellen.](managing-installation-sources.md)

 

 



