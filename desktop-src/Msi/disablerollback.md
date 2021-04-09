---
description: Wenn diese System Richtlinie auf 1 festgelegt ist, speichert das Installationsprogramm während der Installation keine Rollback-Dateien und deaktiviert das Installations Rollback.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DISABLEROLLBACK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959081"
---
# <a name="disablerollback"></a>DISABLEROLLBACK

Wenn diese [System Richtlinie](system-policy.md) auf 1 festgelegt ist, speichert das Installationsprogramm während der Installation keine Rollback-Dateien und deaktiviert das Installations Rollback. Standardmäßig ist das Rollback aktiviert. Administratoren wird empfohlen, diese Richtlinie nicht zu verwenden, es sei denn, Sie ist unbedingt erforderlich. Weitere Informationen finden Sie unter [Rollback-Installation](rollback-installation.md).

## <a name="registry-key"></a>Registrierungsschlüssel

Um das Rollback für Installationen pro Benutzer zu deaktivieren, legen Sie **DISABLEROLLBACK** unter dem folgenden Registrierungsschlüssel auf 1 fest:

**HKEY \_ Aktuelle \_** Richtlinien für Benutzer \\ **Software** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

Um das Rollback für Installationen pro Computer zu deaktivieren, legen Sie **DISABLEROLLBACK** unter dem folgenden Registrierungsschlüssel auf 1 fest.

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 



