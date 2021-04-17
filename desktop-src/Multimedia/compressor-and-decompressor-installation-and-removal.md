---
title: Installation und Deinstallation von Kompressor und Debug
description: Installation und Deinstallation von Kompressor und Debug
ms.assetid: 1f00d86f-a777-4bf8-8290-96cc83b2f331
keywords:
- Videokomprimierungs-Manager (VCM), Installieren von Kompressoren
- VCM (Videokomprimierungs-Manager), Installieren von Kompressoren
- Icinstall-Funktion
- Ikremove-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd65f0fc06dc1d5e90cb136f5cf4ea429c220d77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314708"
---
# <a name="compressor-and-decompressor-installation-and-removal"></a>Installation und Deinstallation von Kompressor und Debug

Eine Anwendung kann Kompressoren und Dekompressoren verwenden, die bereits auf einem System installiert sind, auf dem das Betriebssystem Microsoft Windows ausgeführt wird. Eine Anwendung kann auch Kompressoren und Debug-Funktionen für allgemeine oder spezielle Verwendungszwecke installieren. Die meisten Anwendungen müssen keine Kompressoren installieren oder entfernen, da Sie normalerweise von einem Setup Programm installiert werden. Eine Anwendung kann jedoch einen Kompressor direkt installieren oder eine Funktion als Kompressor installieren.

Eine Anwendung kann mithilfe der Funktion [**icinstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) einen Kompressor oder einen Debug (oder eine Funktion, die als Kompressor oder Debug verwendet wird) installieren. Mit dieser Funktion wird ein Eintrag in der Registrierung erstellt, der den Kompressor oder den Debug identifiziert. Ihre Anwendung oder eine andere Anwendung kann die Registrierung durchsuchen, um festzustellen, ob das System einen für die Daten geeigneten Kompressor oder einen für die Daten geeigneten Debug enthält. Verwenden Sie **icinstall** , um alle Komprimierungs-und Komprimierungs Treiber zu installieren.

Eine Anwendung kann einen installierten Kompressor oder Dekompressor mithilfe der [**iclocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) -Funktion und der [**icopen**](/windows/desktop/api/Vfw/nf-vfw-icopen) -Funktion suchen und öffnen. Wenn eine Anwendung mit einem-Kompressor oder-Debug abgeschlossen ist, wird Sie mithilfe der [**icclose**](/windows/desktop/api/Vfw/nf-vfw-icclose) -Funktion geschlossen.

Eine Anwendung kann den Registrierungs Eintrag für einen installierten Kompressor oder Debug mithilfe der [**ikremove**](/windows/desktop/api/Vfw/nf-vfw-icremove) -Funktion entfernen. Diese Funktion entfernt den Registrierungs Eintrag eines Kompressors oder dekompressors, der derzeit nicht im Arbeitsspeicher geladen ist.

Eine Anwendung kann die Verwendung eines-Kompressors oder-Decoders beschränken, indem Sie installiert, geöffnet, geschlossen und entfernt wird.

Alternativ kann eine Anwendung die [**icopenfunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction) -Funktion verwenden, um eine Funktion intern als Kompressor oder Debug zu verwenden, ohne Sie in der Registrierung zu installieren. Diese Funktion erfordert, dass die aufrufende Anwendung über die Adresse der Funktion verfügt, die als Kompressor oder Dekompressor verwendet werden soll. Wenn die Anwendung mit der-Funktion beendet wird, muss Sie mithilfe von **icclose** geschlossen werden. Da die Funktion nicht installiert wurde, muss die Anwendung die Funktion nicht aus der Registrierung entfernen.

Die interne Struktur einer Funktion, die als Kompressor oder Debug verwendet wird, sollte mit der von installierbaren Treibern verwendeten [driverproc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) -Einstiegspunkt Funktion identisch sein. Weitere Informationen zur **driverproc** -Einstiegspunkt Funktion finden Sie unter [installierbare Treiber](installable-drivers.md).

> [!Note]  
> Eine Anwendung, die eine Funktion als Kompressor oder debug installiert, muss die Funktion entfernen, bevor die Anwendung geschlossen wird, sodass andere Anwendungen nicht versuchen, die Funktion zu verwenden. Beim Entfernen einer Funktion muss Sie von der Anwendung mit dem vierstelligen Code identifiziert werden, der für die Installation verwendet wird.

 

 

 