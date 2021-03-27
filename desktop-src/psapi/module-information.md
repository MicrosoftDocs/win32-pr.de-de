---
title: Modulinformationen
description: Ein Modul ist eine ausführbare Datei oder dll.
ms.assetid: e15b5e15-ca06-4733-bd0a-705058ba2db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625877832b7e57e68ec6baff79f0c34b4478176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390424"
---
# <a name="module-information"></a>Modulinformationen

Ein *Modul* ist eine ausführbare Datei oder dll. Jeder Prozess besteht aus einem oder mehreren Modulen. Sie können die Liste der Modul Handles für einen Prozess abrufen, indem Sie die [**enumprocessmodules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) -Funktion aufrufen. Diese Funktion füllt ein Array von **HMODULE** -Werten mit den Modul Handles für den angegebenen Prozess auf. Das erste Modul ist die ausführbare Datei. Beachten Sie, dass diese Modul Handles wahrscheinlich von einem anderen Prozess verarbeitet werden, sodass Sie Sie nicht mit Funktionen wie [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)verwenden können. Sie können jedoch [PSAPI-Funktionen](psapi-functions.md) verwenden, um Informationen zu einem Modul von einem anderen Prozess abzurufen.

Im folgenden Verfahren wird beschrieben, wie Modul Informationen von einem anderen Prozess abgerufen werden.

**So rufen Sie Modul Informationen von einem anderen Prozess ab**

1.  Aufrufen der [**getmodulebasename**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) -Funktion. Diese Funktion nimmt ein Prozess handle und ein Modul Handle als Eingabe und füllt einen Puffer mit dem Basisnamen eines Moduls (z. b. Kernel32.dll). Die verknüpfte Funktion [**getmoduledatameex**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa)übernimmt dieselben Parameter wie die Eingabe, gibt jedoch den vollständigen Pfad zum Modul zurück (z. b. C: \\ Windows \\ system32 \\Kernel32.dll).
2.  Aufrufen der [**getmoduleinformation**](/windows/desktop/api/Psapi/nf-psapi-getmoduleinformation) -Funktion. Diese Funktion nimmt ein Prozess handle und ein Modul Handle an und füllt eine [**ModuleInfo**](/windows/desktop/api/Psapi/ns-psapi-moduleinfo) -Struktur mit der Lade Adresse des Moduls, der Größe des belegten linearen Adressraums und einem Zeiger auf den Einstiegspunkt.

Wenn eine Anwendung Modul Informationen für den aktuellen Prozess erfordert, sollte Sie die [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) -Funktion anstelle der PSAPI-Modulfunktionen verwenden. Dies unterstützt die Anwendungsleistung auf zwei Arten: die **GetModuleFileName** -Funktion ist effizienter als die PSAPI-Modulfunktionen, und eine Anwendung kann das Laden von psapi.dll vermeiden, wenn keine PSAPI-Funktionen verwendet werden.

Die Funktionen [**getmodulebasename**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) und [**getmoduledateinameex**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) sind hauptsächlich für die Verwendung durch Debugger und ähnliche Anwendungen konzipiert, die Modul Informationen aus einem anderen Prozess extrahieren müssen. Wenn die Modulliste im Ziel Prozess beschädigt ist oder noch nicht initialisiert wurde oder wenn sich die Modulliste während des Funktions Aufrufes ändert, da DLLs geladen oder entladen werden, können diese Funktionen fehlschlagen oder falsche Informationen zurückgeben.

 

 