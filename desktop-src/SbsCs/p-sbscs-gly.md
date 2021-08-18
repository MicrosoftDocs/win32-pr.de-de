---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (Isolierte Anwendungen und nebeneinander seitige Assemblys)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc8e3d2591cfa1544ce11045f95df42e4a27d39b4a2b40d09bc3f2c907c2abec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142013"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a>P (Isolierte Anwendungen und nebeneinander seitige Assemblys)

[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**Anwendungsspezifische Konfiguration**
</dt> <dd>

Konfiguration, die die globale Anwendungskonfiguration einer bestimmten Assembly überschreiben kann. Eine anwendungsspezifische Konfiguration wird von einer Anwendungskonfigurationsmanifestdatei angegeben, die im gleichen Ordner wie die ausführbare Datei installiert ist. Die Manifestdatei beschreibt die Version oder den Bereich von Versionen von nebenseitigen Assemblys, die von der Anwendung verwendet werden sollen. Die Anwendungsspezifische Konfiguration kann verwendet werden, wenn eine neue Version einer Assembly nicht mit einer Anwendung kompatibel ist. In diesem Fall kann die Standardkonfiguration der Anwendung oder die globale Konfiguration für eine bestimmte side-by-side-Assembly überschrieben werden.

</dd> <dt>

<span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**Private side-by-side-Assembly**
</dt> <dd>

Eine private, seite-an-Seite-Assembly ist nur für eine angegebene Anwendung sichtbar. Sie wird lokal in einer isolierten Anwendung installiert, und der Code der Assembly wird für den Anwendungskontext privat. Die Abhängigkeiten einer privaten, seite-an-Seite-Assembly werden in der Anwendungsmanifestdatei beschrieben. Private, nebenseitige Assemblys können verwendet werden, um die negativen Auswirkungen der Assemblyfreigabe wie DLL-Konflikte zu kompensieren und die Anwendungsbereitstellung zu erleichtern.

</dd> <dt>

<span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**Öffentliches Schlüsseltoken**
</dt> <dd>

Eine hexadezimale Zeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Assembly signiert ist. Der öffentliche Schlüssel, der zum Signieren des Katalogs verwendet wird, muss mindestens 2.048 Bit groß sein. Erforderlich für alle freigegebenen, nebenseitigen Assemblys.

</dd> </dl>

 

 



