---
title: Mittel l-Compilerausgabe
description: Wenn die IDL-und ACF-Dateien als Eingabe erstellt werden, generiert der-compilercompiler bis zu fünf Quelldateien der C-Sprache.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb45bb369ea9d5faa695bf2658f3bafe2b3cb3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036596"
---
# <a name="midl-compiler-output"></a>Mittel l-Compilerausgabe

Wenn die IDL-und ACF-Dateien als Eingabe erstellt werden, generiert der-compilercompiler bis zu fünf Quelldateien der C-Sprache. Standardmäßig verwendet der mittlerer l-Compiler den Basis Dateinamen der IDL-Datei als Teil der generierten Stubdateien. Wenn im Basis Dateinamen mehr als sechs Zeichen vorhanden sind, akzeptieren einige Dateisysteme möglicherweise nicht den vollständigen Stub-Namen. In der folgenden Tabelle sind die für Dateinamen verwendeten Konventionen aufgeführt.



| File        | Standardabschnitt des Basis Dateinamens | Beispiel      |
|-------------|-----------------------------------|--------------|
| IDL-Datei    | ---                               | ABCDEFGH. idl |
| Header      | .h                                | Abcdef. h     |
| Clientstub | \_c. c                             | Abcdef \_ c. c  |
| Server-Stub | \_s. c                             | Abcdef \_ s. c  |



 

 

 




