---
description: Es gibt eine Reihe interessanter Abfragen für einen Treiber, die eine Anwendung ausführen kann, wenn es keine Leistungskosten gibt.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Asynchrone Benachrichtigung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd23a64e613bbbae56154dc35c05bcf08b75c4c91f306360153e775e12c40ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123417"
---
# <a name="asynchronous-notification-direct3d-9"></a>Asynchrone Benachrichtigung (Direct3D 9)

Es gibt eine Reihe interessanter Abfragen für einen Treiber, die eine Anwendung ausführen kann, wenn es keine Leistungskosten gibt. In Direct3D 7 und Direct3D 8 funktionierte der synchrone Abfragemechanismus GetInfo gut für Dinge wie Statistiken, aber es wurden keine leistungskritischen Abfragen hinzugefügt. Es gibt andere Dinge (z. B. Zäunen), die grundsätzlich asynchron sind. Dies ist eine einfache API, um sowohl synchrone als auch asynchrone Abfragen zu erstellen. GetInfo wird in Direct3D 9 zurückgezogen.

Erstellen Sie eine Abfrage [**mithilfe von IDirect3DDevice9::CreateQuery**](/windows/desktop/api). Diese Methode verwendet einen D3DQUERYTYPE, der definiert, welche Art von Abfrage ausgeführt werden soll, und gibt einen Zeiger auf ein [**IDirect3DQuery9-Objekt**](/windows/desktop/api) zurück. Wenn der Abfragetyp nicht unterstützt wird, gibt der Aufruf den Fehler D3DERR \_ NOTAVAILABLE zurück. Mithilfe des Abfrageobjekts übermittelt die Anwendung die Abfrage mithilfe von [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)an die Laufzeit und abruft den Abfragestatus mithilfe von [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Wenn das Abfrageergebnis verfügbar ist, wird S \_ OK zurückgegeben, andernfalls wird S \_ FALSE zurückgegeben. Es wird erwartet, dass die Anwendung einen Puffer mit entsprechender Größe für die Abfrageergebnisse über gibt.

Die Anwendung verfügt über eine Option, die Laufzeit zu zwingen, die Abfrage mithilfe von D3DGETDATA FLUSH mit \_ [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)an den Treiber zu leeren. Dies führt zu einer Leerung, die den Treiber zwingt, die Abfrage zu sehen. In diesem Fall wird D3DERR DEVICELOST zurückgegeben, \_ wenn das Gerät verloren geht.

Alle Abfragen gehen verloren, wenn das Gerät verloren geht. Die Anwendung muss sie neu erstellen. Wenn das Gerät die Abfrage nicht unterstützt und die pQueryID **NULL ist,** kann die Abfrage nicht mit D3DERR \_ INVALIDCALL erstellt werden.

In der folgenden Tabelle werden wichtige Informationen zu den einzelnen Abfragetypen zusammengefasst.



| QuertyType                    | Gültiges Problemflag              | GetData-Puffer              | Typ      | Impliziter Anfang der Abfrage |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| D3DQUERYTYPE \_ VCACHE          | D3DISSUE \_ END                 | D3DDEVINFO \_ VCACHE          | Einzelhandel/Debuggen | CreateDevice                |
| D3DQUERYTYPE \_ ResourceManager | D3DISSUE \_ END                 | D3DDEVINFO \_ ResourceManager | Nur Debuggen   | Anzahl                     |
| D3DQUERYTYPE \_ VERTEXSTATS     | D3DISSUE \_ END                 | D3DDEVINFO \_ D3DVERTEXSTATS  | Nur Debuggen   | Anzahl                     |
| D3DQUERYTYPE-EREIGNIS \_           | D3DISSUE \_ END                 | BOOL                        | Einzelhandel/Debuggen | CreateDevice                |
| D3DQUERYTYPE \_ OCCLUSION       | D3DISSUE \_ BEGIN,D3DISSUE \_ END | DWORD                       | Einzelhandel/Debuggen | Nicht zutreffend                         |



 

Flags-Feld für [**IDirect3DQuery9::Issue:**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



Flags-Feld für [**IDirect3DQuery9::GetData:**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren Tipps](programming-tips.md)
</dt> </dl>

 

 
