---
title: Grundlagen zu Primieren und Dekomprimieren
description: Grundlagen zu Primieren und Dekomprimieren
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- Videokomprimierungs-Manager (Video Compression Manager, VCM), Öffnen von Komprimierungsdateien
- VCM (Videokomprimierungs-Manager), öffnende Komprimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1969748949aeb023f889bc651ccd028f19c3e18fe6cf1ba088b4f4ec29292f35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144993"
---
# <a name="compressor-and-decompressor-basics"></a>Grundlagen zu Primieren und Dekomprimieren

Um eine Hülle zu öffnen und zu suchen, können Sie die [**Funktionen ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) und [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) verwenden. Sie können **ICLocate verwenden,** um einen Bestimmten Typ zu finden und ein Handle dafür für die Verwendung in anderen VCM-Funktionen zu erhalten. Um eine Hülle zu öffnen, können Sie **ICOpen verwenden.** Ihre Anwendung verwendet das von dieser Funktion zurückgegebene Handle, um die geöffnete Komprimierung zu identifizieren, wenn sie andere VCM-Funktionen verwendet.

Um einen Dekomprimator zu öffnen und zu suchen, können Anwendungen die [**Makros ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) und [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) verwenden. Diese Makros verwenden **ICLocate für** den Vorgang.

Wenn Ihre Anwendung die Verwendung eines Komprimierungs- oder Dekomprimierers beendet hat, muss sie sie schließen, um alle Ressourcen frei zu geben, die für die Komprimierung oder Dekomprimierung verwendet werden. Ihre Anwendung kann die [**ICClose-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icclose) verwenden, um den Schließ- oder Dekomprimierer zu schließen.

Darüber hinaus kann Ihre Anwendung mithilfe der ICInfo-Funktion die Komprimierungs- oder Dekomprimierungsfunktionen auf einem [**System aufzählen.**](/windows/desktop/api/Vfw/nf-vfw-icinfo)

> [!Note]  
> Der Streamheader in einer AVI-Datei enthält Informationen über den Streamtyp und den spezifischen Handler für diesen Stream. Innerhalb des Streamheaders identifizieren **die Elemente fccType** und **fccHandler** den Streamtyp und den für den Stream angegebenen Streamhandler.

 

 

 




