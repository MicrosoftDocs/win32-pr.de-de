---
description: Um eine Datei zu signieren und einen Katalog dafür zu erstellen, benötigen Sie zunächst einen Prozess zum Signieren von Dateien, ein Zertifikat und einen öffentlichen Schlüssel.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Erstellen von signierten Dateien und Katalogen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9abcccc2451cfa9461bc8129705c1094291b33fea609679c89ef46d7cf7348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142323"
---
# <a name="creating-signed-files-and-catalogs"></a>Erstellen von signierten Dateien und Katalogen

Um eine Datei zu signieren und einen Katalog dafür zu erstellen, benötigen Sie zunächst einen Prozess zum Signieren von Dateien, ein Zertifikat und einen öffentlichen Schlüssel.

**So signieren Sie eine Datei und erstellen einen Katalog**

1.  Verwenden Sie [Pktextract.exe,](pktextract-exe.md) um das [*öffentliche Schlüsseltoken*](p-sbscs-gly.md) aus der Zertifikatdatei zu extrahieren. Die Zertifikatdatei muss sich im gleichen Verzeichnis wie das Hilfsprogramm befinden.
2.  Verwenden Sie den Wert des öffentlichen Schlüsseltokens, um das **publicKeyToken-Attribut** des **assemblyIdentity-Elements** in der Manifestdatei zu aktualisieren.
3.  Verwenden Sie [MT.exe, ](mt-exe.md) um Hashes von Dateien zu generieren, die im Assemblymanifest enthalten sind, und um die Katalogbeschreibungsdatei (CDF) zu erstellen.
4.  Verwenden Sie Makecat.exe mit der generierten CDF-Datei, um den Sicherheitskatalog für die Assembly zu erstellen. Dieses Tool ist in der CryptoAPI enthalten.
5.  Verwenden Sie das [Hilfsprogramm SignTool,](/windows/desktop/SecCrypto/signtool) um den Katalog zu signieren, der mit dem in Schritt 1 verwendeten Zertifikat generiert wurde. Die CDF-Datei aus den Schritten 3 und 4 kann gelöscht werden, nachdem der Katalog erstellt wurde.

Siehe auch [AssemblySignierungsbeispiel.](assembly-signing-example.md)

 

 
