---
description: Zum Signieren einer Datei und zum Erstellen eines Katalogs müssen Sie zunächst über einen Prozess zum Signieren von Dateien, ein Zertifikat und einen öffentlichen Schlüssel verfügen.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Erstellen signierter Dateien und Kataloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216344"
---
# <a name="creating-signed-files-and-catalogs"></a>Erstellen signierter Dateien und Kataloge

Zum Signieren einer Datei und zum Erstellen eines Katalogs müssen Sie zunächst über einen Prozess zum Signieren von Dateien, ein Zertifikat und einen öffentlichen Schlüssel verfügen.

**So signieren Sie eine Datei und erstellen einen Katalog**

1.  Verwenden Sie [Pktextract.exe](pktextract-exe.md) , um das [*öffentliche Schlüssel Token*](p-sbscs-gly.md) aus der Zertifikatsdatei zu extrahieren. Die Zertifikatsdatei muss sich im selben Verzeichnis wie das-Hilfsprogramm befinden.
2.  Verwenden Sie den Wert des öffentlichen Schlüssel Tokens, um das **PublicKeyToken** -Attribut des **assemblyIdentity** -Elements in der Manifest-Datei zu aktualisieren.
3.  Verwenden Sie [MT.exe](mt-exe.md) , um Hashwerte von Dateien zu generieren, die im Assemblymanifest enthalten sind, und um die Katalog Beschreibungsdatei (CDF) zu erstellen.
4.  Verwenden Sie Makecat.exe mit der generierten CDF-Datei, um den Sicherheits Katalog für die Assembly zu erstellen. Dieses Tool ist in der CryptoAPI enthalten.
5.  Verwenden Sie das Hilfsprogramm [SignTool](/windows/desktop/SecCrypto/signtool) zum Signieren des Katalogs, der mit dem in Schritt 1 verwendeten Zertifikat generiert wurde. Die CDF aus den Schritten 3 und 4 können gelöscht werden, nachdem der Katalog erstellt wurde.

Siehe auch [Beispiel für Assemblysignierung](assembly-signing-example.md).

 

 
