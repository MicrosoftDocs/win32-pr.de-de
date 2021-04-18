---
description: Es gibt zahlreiche interessante Abfragen für einen Treiber, die eine Anwendung ausführen kann, wenn keine Leistungskosten anfallen.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Asynchrone Benachrichtigung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343601"
---
# <a name="asynchronous-notification-direct3d-9"></a>Asynchrone Benachrichtigung (Direct3D 9)

Es gibt zahlreiche interessante Abfragen für einen Treiber, die eine Anwendung ausführen kann, wenn keine Leistungskosten anfallen. In Direct3D 7 und Direct3D 8 hat ein synchroner Abfrage Mechanismus GetInfo für Dinge wie Statistiken gut funktioniert, aber es wurden keine Leistungs kritischen Abfragen hinzugefügt. Es gibt noch andere Dinge (wie z. b. Zäune), die grundsätzlich asynchron sind. Dies ist eine einfache API, mit der synchrone und asynchrone Abfragen durchführen werden. GetInfo wird in Direct3D 9 eingestellt.

Erstellen Sie eine Abfrage mit [**IDirect3DDevice9:: kreatequery**](/windows/desktop/api). Diese Methode nimmt ein D3DQUERYTYPE-Objekt an, das definiert, welche Art von Abfrage durchführen werden soll, und gibt einen Zeiger auf ein [**IDirect3DQuery9**](/windows/desktop/api) -Objekt zurück. Wenn der Abfragetyp nicht unterstützt wird, gibt der Aufruf einen Fehler zurück D3DERR \_ NotAvailable. Mithilfe des Query-Objekts übermittelt die Anwendung die Abfrage mithilfe von [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)an die Laufzeit und fragt den Abfrage Status mithilfe von [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)ab. Wenn das Abfrageergebnis verfügbar ist, \_ wird s OK zurückgegeben; andernfalls \_ wird s false zurückgegeben. Es wird erwartet, dass die Anwendung einen entsprechend großen Puffer für die Abfrageergebnisse übergibt.

Die Anwendung verfügt über eine Option, mit der die Laufzeit gezwungen wird, die Abfrage mithilfe von D3DGETDATA \_ Flush mit [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)an den Treiber zu leeren. Dies bewirkt eine Leerung und erzwingt den Treiber, die Abfrage anzuzeigen. In diesem Fall wird D3DERR \_ DeviceLost zurückgegeben, wenn das Gerät verloren geht.

Alle Abfragen gehen verloren, wenn das Gerät verloren geht, und die Anwendung muss Sie neu erstellen. Wenn die Abfrage vom Gerät nicht unterstützt wird und pqueryid **null** ist, schlägt die Erstellung der Abfrage mit D3DERR \_ invalidcallfehl.

In der folgenden Tabelle werden wichtige Informationen zu den einzelnen Abfrage Typen zusammengefasst.



| Quertytype                    | Gültiges Issue-Flag              | GetData-Puffer              | Typ      | Impliziter Beginn der Abfrage |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| D3DQUERYTYPE \_ VCACHE          | D3DISSUE \_ Ende                 | D3DDEVINFO \_ VCACHE          | Retail/Debug | "Kreatedevice"                |
| D3DQUERYTYPE \_ ResourceManager | D3DISSUE \_ Ende                 | D3DDEVINFO \_ ResourceManager | Nur Debuggen   | Anzahl                     |
| D3DQUERYTYPE \_ vertexstats     | D3DISSUE \_ Ende                 | D3DDEVINFO \_ D3DVERTEXSTATS  | Nur Debuggen   | Anzahl                     |
| D3DQUERYTYPE- \_ Ereignis           | D3DISSUE \_ Ende                 | BOOL                        | Retail/Debug | "Kreatedevice"                |
| D3DQUERYTYPE- \_ oksion       | D3DISSUE \_ Begin, D3DISSUE \_ End | DWORD                       | Retail/Debug | –                         |



 

Flags-Feld für [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



Flags-Feld für [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmiertipps](programming-tips.md)
</dt> </dl>

 

 
