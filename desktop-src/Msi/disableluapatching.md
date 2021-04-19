---
description: Wenn diese pro-Computer-System Richtlinie auf &\# 0034; 1&0034; festgelegt ist \# , verhindert das Installationsprogramm, dass nicht Administratoren die Benutzerkontensteuerung (User Account Control, UAC) für alle auf dem Computer installierten Anwendungen verwenden.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: Disableluapatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355079"
---
# <a name="disableluapatching"></a>Disableluapatching

Wenn diese pro-Computer-System Richtlinie auf "1" festgelegt ist, verhindert das Installationsprogramm, dass nicht Administratoren die [Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md) für alle auf dem Computer installierten Anwendungen verwenden. Wenn die System Richtlinie pro Computer nicht festgelegt oder auf 0 festgelegt ist, können nicht Administratoren benutzerpatches mit geringsten Rechten auf Anwendungen anwenden, die für das Patchen von Benutzerkonten mit geringsten Rechten aktiviert sind.

Verwenden Sie die [**msidisableluapatching**](msidisableluapatching.md) -Eigenschaft, um das Patchen einer Anwendung mit den geringsten Berechtigungen zu verhindern.

Die Richtlinie "disableluapatching" ist ab Windows Installer Version 3,0 verfügbar.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



