---
description: Pktextract.exe ist ein Tool, das das PublicKeyToken-Attribut aus einer Zertifikatsdatei extrahiert.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd163efabd01d65969788aefc2386b2f49079729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131301"
---
# <a name="pktextractexe"></a>Pktextract.exe

Pktextract.exe ist ein Tool, das das **PublicKeyToken** -Attribut aus einer Zertifikatsdatei extrahiert. Bei der Ausgabe handelt es sich um das **PublicKeyToken**, bei dem es sich um einen eindeutigen 16-Byte-Bezeichner (8-Byte) des öffentlichen Schlüssels handelt, der im Zertifikat vorhanden ist, in einem Format, das leicht in eine Assembly-Identitäts Anweisung eingefügt werden kann. Die Zertifikatsdatei muss sich im selben Verzeichnis wie Pktextract.exe befinden, um das Hilfsprogramm zu verwenden. Pktextract.exe wird im Microsoft Windows Software Development Kit (SDK) bereitgestellt.

## <a name="syntax"></a>Syntax

**pktextract.exe** *<filename. CER>* **\[ -quiet \] \[ -nologo \]**

## <a name="command-line-options"></a>Befehlszeilenoptionen

Pktextract.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung.



| Option  | BESCHREIBUNG                                                          |
|---------|----------------------------------------------------------------------|
| -quiet  | Unterdrückt die vollständige Anzeige von Zertifikat Informationen. Dies ist optional.        |
| -nologo | Wird ohne Anzeige der standardmäßigen Microsoft-Copyright Daten ausgeführt. Dies ist optional. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Parallele assemblyentwicklungtools](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



