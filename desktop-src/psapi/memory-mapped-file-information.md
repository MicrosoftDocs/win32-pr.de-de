---
title: Dateiinformationen Memory-Mapped
description: Eine im Speicher abgebildete Datei (oder Datei Zuordnung) ist das Ergebnis der Zuordnung des Inhalts einer Datei zu einem Teil des virtuellen Adressraums eines Prozesses. Sie kann verwendet werden, um eine Datei oder einen Arbeitsspeicher zwischen zwei oder mehr Prozessen freizugeben.
ms.assetid: b6ec2bc4-c504-4d0b-87f0-39bb1949accd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc6d33e7f3fe6bef36ea6e5a7f355b780d89b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102162"
---
# <a name="memory-mapped-file-information"></a>Dateiinformationen Memory-Mapped

Eine im *Speicher abgebildete Datei* (oder *Datei Zuordnung*) ist das Ergebnis der Zuordnung des Inhalts einer Datei zu einem Teil des virtuellen Adressraums eines Prozesses. Sie kann verwendet werden, um eine Datei oder einen Arbeitsspeicher zwischen zwei oder mehr Prozessen freizugeben.

Die [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) -Funktion empfängt ein Prozess handle und einen Zeiger auf eine Adresse als Eingabe. Wenn sich die Adresse innerhalb einer Speicher Abbild Datei im virtuellen Adressraum des Prozesses befindet, gibt die Funktion den Namen der Speicher Abbild Datei zurück. Die von **GetMappedFileName** zurückgegebenen Dateinamen verwenden Geräte Form anstelle von Laufwerk Buchstaben. Beispielsweise sieht der Dateiname "c: \\ Winnt \\ system32 \\ CType. nls" in Geräte Form wie folgt aus:

\\Device \\ Harddisk0 \\ Partition1 \\ Winnt \\ system32 \\ CType. nls

Weitere Informationen zu Speicher Abbild Dateien finden Sie unter [Datei Zuordnung](/windows/desktop/Memory/file-mapping). Ein Beispiel für das Konvertieren von Dateinamen in Geräte Form in Laufwerk Buchstaben finden Sie unter Abrufen [eines Datei namens aus einem Datei Handle](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).

 

 