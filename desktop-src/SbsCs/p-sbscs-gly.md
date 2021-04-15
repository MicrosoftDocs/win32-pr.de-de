---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (isolierte Anwendungen und parallele Assemblys)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c70c0775af4a6245e74de474413c3741625456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393358"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a>P (isolierte Anwendungen und parallele Assemblys)

[a](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**Konfiguration pro Anwendung**
</dt> <dd>

Konfiguration, die die globale Anwendungskonfiguration einer bestimmten Assembly überschreiben kann. Eine anwendungsspezifische Konfiguration wird durch eine Anwendungs konfigurationsmanifest-Datei angegeben, die im selben Ordner wie die ausführbare Datei installiert ist. Die Manifest-Datei beschreibt die Version bzw. den Bereich der Versionen von parallelen Assemblys, die von der Anwendung verwendet werden sollen. Die Konfiguration pro Anwendung kann verwendet werden, wenn eine neue Version einer Assembly nicht mit einer Anwendung kompatibel ist. In diesem Fall kann die standardmäßige oder globale Konfiguration der Anwendung für eine bestimmte parallele Assembly überschrieben werden.

</dd> <dt>

<span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**private parallele Assembly**
</dt> <dd>

Eine private parallele Assembly ist nur für eine bestimmte Anwendung sichtbar. Sie wird lokal in einer isolierten Anwendung installiert, und der Assemblycode wird für den Anwendungskontext privat. Die Abhängigkeiten einer privaten parallelen Assembly werden in der Anwendungs Manifest-Datei beschrieben. Private parallele Assemblys können verwendet werden, um die negativen Auswirkungen der assemblyfreigabe (z. b. dll-Konflikte) auszugleichen und die Anwendungs Bereitstellung zu vereinfachen.

</dd> <dt>

<span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**öffentliches Schlüssel Token**
</dt> <dd>

Eine hexadezimale Zeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Assembly signiert ist. Der öffentliche Schlüssel, der zum Signieren des Katalogs verwendet wird, muss 2048 Bit oder größer sein. Erforderlich für alle freigegebenen parallelen Assemblys.

</dd> </dl>

 

 



