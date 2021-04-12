---
description: Windows Installer wird als Dienst auf Computern mit 32-Bit-oder 64-Bit-Windows ausgeführt.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: Informationen zu Windows Installer auf 64-Bit-Betriebssystemen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "104218865"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a>Informationen zu Windows Installer auf 64-Bit-Betriebssystemen

Windows Installer wird als Dienst auf Computern mit 32-Bit-oder 64-Bit-Windows ausgeführt. Versionen des Installationsprogramms vor Version 2,0 können 32-Bit-Windows Installer Pakete nur unter 32-Bit-Betriebssystemen installieren und verwalten. Beachten Sie, dass Sie eine 64-Bit-Anwendung auf einem 32-Bit-Betriebssystem nicht ankündigen oder installieren können.

Ein Windows Installer Paket muss entweder als 32-Bit-oder als 64-Bit-Paket angegeben werden. Er kann nicht als neutral angegeben werden. Auf einem Computer, der ein 64-Bit-Betriebssystem verwendet, wird der Windows Installer-Dienst in einem 64-Bit-Prozess gehostet, der sowohl 32-Bit-als auch 64-Bit-Pakete installiert. Von Windows Installer werden drei Typen von Windows Installer-Paketen auf einem Computer installiert, auf dem ein 64-Bit-Betriebssystem ausgeführt wird:

-   32-Bit-Pakete, die nur 32-Bit-Komponenten enthalten.
-   64-Bit-Pakete, die einige 32-Bit-Komponenten enthalten.
-   64-Bit-Pakete, die nur 64-Bit-Komponenten enthalten.

In den folgenden Abschnitten werden die beiden Typen von Windows Installer Paketen und die neuen Installer-Eigenschaften beschrieben, die von Windows Installer für 64-Bit-Pakete bereitgestellt werden.

[32-Bit-Windows Installer Pakete](32-bit-windows-installer-packages.md)

[64-Bit-Windows Installer Pakete](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von 64-Bit-Windows Installer Paketen](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



