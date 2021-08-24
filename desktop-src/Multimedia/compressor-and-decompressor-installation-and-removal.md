---
title: Installations- und Dekomprimierungs- und Dekomprimierungsvorgang
description: Installations- und Dekomprimierungs- und Dekomprimierungsvorgang
ms.assetid: 1f00d86f-a777-4bf8-8290-96cc83b2f331
keywords:
- Videokomprimierungs-Manager (VCM), Installieren von Reparaturen
- VCM (Videokomprimierungs-Manager),Installieren von Schlägen
- ICInstall-Funktion
- ICRemove-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82a34f1818f9a60226c0f3cead8186ae3fa163ebe1782c0c83e7cfb5b633c1b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144981"
---
# <a name="compressor-and-decompressor-installation-and-removal"></a>Installations- und Dekomprimierungs- und Dekomprimierungsvorgang

Eine Anwendung kann Leitungen und Dekomprimierer verwenden, die bereits auf einem System installiert sind, auf dem microsoft Windows Betriebssystem ausgeführt wird. Eine Anwendung kann auch Installierungs- und Dekomprimierer für allgemeine oder spezielle Zwecke installieren. Die meisten Anwendungen müssen keine Entpackungen oder Dekomprimierer installieren oder entfernen, da sie in der Regel von einem Setupprogramm installiert werden. Eine Anwendung kann jedoch direkt eine Pumpe installieren oder eine Funktion als 160000000000000000000000000000000000000000

Eine Anwendung kann mithilfe der [**ICInstall-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icinstall) einen Druck- oder Dekomprimierer installieren (oder eine Funktion, die als Trenn- oder Dekomprimierungsfunktion verwendet wird). Diese Funktion erstellt einen Eintrag in der Registrierung, der den Entpacker oder Dekomprimierer identifiziert. Ihre Anwendung oder eine andere Anwendung kann die Registrierung durchsuchen, um zu ermitteln, ob das System einen für die Daten geeigneten Dekomprimierer enthält. Verwenden Sie **ICInstall,** um alle Komprimierungs- und Dekomprimierungstreiber zu installieren.

Eine Anwendung kann mithilfe der Funktionen [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) und [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) einen installierten Entpacker oder Dekomprimierer suchen und öffnen. Wenn eine Anwendung die Verwendung eines Entpackungs- oder Dekomprimierers beendet, wird sie mithilfe der [**ICClose-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icclose) geschlossen.

Eine Anwendung kann den Registrierungseintrag für einen installierten Entpacker oder Dekomprimierer mithilfe der [**ICRemove-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icremove) entfernen. Diese Funktion entfernt den Registrierungseintrag eines Komprimierungs- oder Dekomprimierers, der derzeit nicht in den Arbeitsspeicher geladen ist.

Eine Anwendung kann die Verwendung eines Entpackungs- oder Dekomprimierers einschränken, indem sie installiert, geöffnet, geschlossen und entfernt wird.

Alternativ kann eine Anwendung die [**ICOpenFunction-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction) verwenden, um eine Funktion intern als Aggregat oder Dekomprimierer zu verwenden, ohne sie in der Registrierung zu installieren. Für diese Funktion muss die aufrufende Anwendung über die Adresse der Funktion verfügen, die als Diktat oder Dekomprimierer verwendet werden soll. Wenn die Anwendung die Verwendung der Funktion beendet, muss sie sie mithilfe von **ICClose** schließen. Da die Funktion nicht installiert wurde, muss die Anwendung die Funktion nicht aus der Registrierung entfernen.

Die interne Struktur einer Funktion, die als Zieh- oder Dekomprimierer verwendet wird, sollte mit der [DriverProc-Einstiegspunktfunktion](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) identisch sein, die von installierbaren Treibern verwendet wird. Weitere Informationen zur **DriverProc-Einstiegspunktfunktion** finden Sie unter [Installierbare Treiber.](installable-drivers.md)

> [!Note]  
> Eine Anwendung, die eine Funktion als Lösch- oder Dekomprimierer installiert, muss die Funktion entfernen, bevor die Anwendung geschlossen wird, damit andere Anwendungen nicht versuchen, die Funktion zu verwenden. Beim Entfernen einer Funktion muss die Anwendung sie mit dem vierstelligen Code identifizieren, der für die Installation verwendet wird.

 

 

 