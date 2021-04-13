---
title: Windows-Netzwerk Vorgänge
description: Eine Anwendung kann die WNET-Funktionen zum Durchsuchen, hinzufügen oder Abbrechen von Netzwerkverbindungen überall in der Netzwerk Hierarchie verwenden.
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30326d9ad1299e577c65586cff3df3010c086f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315470"
---
# <a name="windows-networking-operations"></a>Windows-Netzwerk Vorgänge

Eine Anwendung kann die WNET-Funktionen zum Durchsuchen, hinzufügen oder Abbrechen von Netzwerkverbindungen überall in der Netzwerk Hierarchie verwenden.

Eine *permanente Verbindung* ist eine Netzwerkverbindung, die vom System automatisch wieder hergestellt wird, wenn sich der Benutzer anmeldet. Sie können die Funktionen [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (oder [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) und [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) aufzurufen, um zu steuern, ob eine Netzwerkverbindung zwischen einer Sitzung und der nächsten Sitzung persistent ist.

Rufen Sie die [**wnetgetuser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) -Funktion auf, um den Standardbenutzer Namen oder den Benutzernamen zu ermitteln, der zum Herstellen einer Netzwerkverbindung verwendet wird.

Zusätzlich zum Aufrufen der WNET-Funktionen kann ein Prozess auch Mailslots und Named Pipes verwenden, um mit einem anderen Prozess zu kommunizieren. Weitere Informationen finden Sie unter [Mailslots](/windows/desktop/ipc/mailslots) und [Pipes](/windows/desktop/ipc/pipes).

 

 