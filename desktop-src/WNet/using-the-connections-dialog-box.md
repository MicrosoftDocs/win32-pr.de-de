---
title: Verwenden des Dialog Felds "Verbindungen"
description: Die wnetconnectiondialog-Funktion erstellt ein Dialogfeld, in dem der Benutzer Netzwerkressourcen durchsuchen und verbinden kann.
ms.assetid: ef375004-e426-4dee-b318-b470721116fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69d0f32772e614d60598853af620ae3c6452f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315681"
---
# <a name="using-the-connections-dialog-box"></a>Verwenden des Dialog Felds "Verbindungen"

Die [**wnetconnectiondialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) -Funktion erstellt ein Dialogfeld, in dem der Benutzer Netzwerkressourcen durchsuchen und verbinden kann. Sie können auch die [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) -Funktion zum Erstellen eines Verbindungs Dialogfelds aufruft. **WNetConnectionDialog1** erfordert eine [**connectdlgstruct**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) -Struktur.

Die [**wnetdisconnectdialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) -Funktion erstellt ein Dialogfeld, in dem der Benutzer die Verbindung mit Netzwerkressourcen trennen kann.

Im folgenden Codebeispiel wird veranschaulicht, wie die **wnetconnectiondialog** -Funktion aufgerufen wird, um ein Dialogfeld zu erstellen, in dem Datenträger Ressourcen angezeigt werden. Wenn der Aufruf fehlschlägt, wird im Beispiel ein von der Anwendung definierter Fehlerhandler aufgerufen.


```C++
DWORD dwResult; 
//
// Call the WNetConnectionDialog function.
//
dwResult = WNetConnectionDialog(hwnd, RESOURCETYPE_DISK);
//
// Call an application-defined error handler 
//  to process errors.
//
if(dwResult != NO_ERROR) 
{
    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetConnectionDialog"); 
    return FALSE; 
}
```



Weitere Informationen zum Verwenden eines Anwendungs definierten Fehler Handlers finden Sie unter [Abrufen von Netzwerkfehlern](retrieving-network-errors.md).

 

 