---
description: Pktextract.exe ist ein Tool, das das publicKeyToken-Attribut aus einer Zertifikatsdatei extrahiert.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7f2cbb210262a05839ac3a7df71f3bedea603a5ea959249867efc2d5e420e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884954"
---
# <a name="pktextractexe"></a>Pktextract.exe

Pktextract.exe ist ein Tool, das das **publicKeyToken-Attribut** aus einer Zertifikatdatei extrahiert. Die Ausgabe ist das **publicKeyToken,** bei dem es sich um einen eindeutigen 16-Zeichen-Bezeichner (8 Byte) des öffentlichen Schlüssels handelt, der im Zertifikat vorhanden ist, in einem Format, das problemlos in eine Assemblyidentitäts-Anweisung eingefügt werden kann. Die Zertifikatdatei muss sich im gleichen Verzeichnis wie Pktextract.exe befinden, um das Hilfsprogramm verwenden zu können. Pktextract.exe wird im Microsoft Windows Software Development Kit (SDK) bereitgestellt.

## <a name="syntax"></a>Syntax

**pktextract.exe** *<Dateiname.cer>* **\[ -quiet \] \[ -nologo \]**

## <a name="command-line-options"></a>Befehlszeilenoptionen

Pktextract.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird.



| Option  | BESCHREIBUNG                                                          |
|---------|----------------------------------------------------------------------|
| -quiet  | Unterdrückt die vollständige Anzeige von Zertifikatinformationen. Optional.        |
| -nologo | Wird ausgeführt, ohne standardmäßige Microsoft-Copyrightdaten anzuzeigen. Optional. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungstools für die side-by-Side-Assembly](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



