---
title: Der Pipezustand
description: Auf dem-Server erstellt der-compilercompiler eine Zustands Variable, mit der Push-, Pull-und zuordnungsprozeduren koordiniert werden.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d7ec8af1907c98b7cf2098f4979dac62ef573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101946"
---
# <a name="the-pipe-state"></a>Der Pipezustand

Auf dem-Server erstellt der-compilercompiler eine *Zustands* Variable, mit der Push-, Pull-und zuordnungsprozeduren koordiniert werden. Auf der Clientseite muss der Entwickler die *Zustands* Variable erstellen. Daher ist die *Zustands* Variable auf beiden Seiten lokal – d. h., der Client und der Server behalten jeweils ihren eigenen Pipezustand. Der Server-Stub-Code verwaltet die Zustands Variable auf dem Server. Sie sollten nicht versuchen, den Inhalt direkt zu ändern. Der Client muss die Felder in der Pipe-Steuerelement Struktur initialisieren und seine *Zustands* Variable beibehalten. Es verwendet die *State* -Variable, um zu bestimmen, wo Daten gesucht oder platziert werden sollen.

Die Client *Status* Variable kann so einfach wie ein Datei Handle sein, wenn Sie Daten aus einer Datei in eine andere übertragen. Es kann auch eine ganze Zahl sein, die auf ein Element in einem Array verweist. Sie können auch eine recht komplexe Zustands Struktur definieren, um zusätzliche Aufgaben auszuführen, z. b. das Koordinieren der Push-und Pull-Routinen für einen \[ [in](/windows/desktop/Midl/in)-, [out](/windows/desktop/Midl/out-idl) - \] Parameter.

 

 