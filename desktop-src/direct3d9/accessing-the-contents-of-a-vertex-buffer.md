---
description: Vertex-Puffer Objekte ermöglichen Anwendungen den direkten Zugriff auf den für Scheitelpunkt Daten zugewiesenen Arbeitsspeicher.
ms.assetid: 63d255b7-fa7d-411b-9cdb-52113f30c933
title: Zugreifen auf den Inhalt eines Scheitelpunkt Puffers (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b5e4a4986e064d3736f83567f5dd6d479d0dbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346439"
---
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a>Zugreifen auf den Inhalt eines Scheitelpunkt Puffers (Direct3D 9)

Vertex-Puffer Objekte ermöglichen Anwendungen den direkten Zugriff auf den für Scheitelpunkt Daten zugewiesenen Arbeitsspeicher. Sie können einen Zeiger auf den Vertex-Pufferspeicher abrufen, indem Sie die [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) -Methode aufrufen und dann nach Bedarf auf den Speicher zugreifen, um den Puffer mit neuen Scheitelpunkt Daten zu füllen oder um bereits enthaltene Daten zu lesen. Die **IDirect3DVertexBuffer9:: Lock** -Methode akzeptiert vier Parameter. Der erste, *offsetToLock*, ist der Offset in den Scheitelpunkt Daten. Der zweite Parameter ist die Größe der Scheitelpunkt Daten in Bytes. Der dritte akzeptierte Parameter ist die Adresse eines Zeigers, der auf die Scheitelpunkt Daten zeigt, wenn der-Befehl erfolgreich ausgeführt wird.

Der letzte Parameter, *Flags*, teilt dem System mit, wie der Arbeitsspeicher gesperrt werden soll. Geben Sie Konstanten für den *Flags* -Parameter entsprechend der Art und Weise an, wie auf die Vertex-Daten zugegriffen wird. Stellen Sie sicher, dass der für [**D3DUSAGE**](d3dusage.md) gewählte Wert mit dem für [D3DLOCK](d3dlock.md)ausgewählten Wert übereinstimmt. Wenn Sie z. b. einen Vertex-Puffer nur mit Schreibzugriff erstellen, ist es nicht sinnvoll, die Daten zu lesen, indem Sie D3DLOCK Read \_ only angeben. Durch die Verwendung dieser Flags kann der Treiber den Speicher sperren und die beste Leistung bereitstellen, wenn der angeforderte Zugriffstyp vorhanden ist.

Nachdem Sie das Ausfüllen oder Lesen der Scheitelpunkt Daten abgeschlossen haben, können Sie die [**IDirect3DVertexBuffer9:: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) -Methode wie im folgenden Codebeispiel gezeigt abrufen.


```
// This code example assumes the g_pVB is a variable of type 
//   LPDIRECT3DVERTEXBUFFER9 and that g_Vertices has been  
//   properly initialized with vertices

// Lock the buffer to gain access to the vertices 
VOID* pVertices;

if(FAILED(g_pVB->Lock(0, sizeof(g_Vertices), 
        (BYTE**)&pVertices, 0 ) ) ) 
    return E_FAIL;

memcpy(pVertices, g_Vertices, sizeof(g_Vertices));
g_pVB->Unlock();
```



Wenn Sie einen Vertex-Puffer mit dem \_ Flag D3DUSAGE Write only erstellen, verwenden Sie nicht das Sperr Kennzeichen D3DLOCK Read \_ only. Verwenden Sie das D3DLOCK-Flag "schreibgeschützt", \_ Wenn die Anwendung nur aus dem Vertex-Pufferspeicher gelesen wird. Das Einschließen dieses Flags ermöglicht Direct3D, seine internen Prozeduren zu optimieren, um die Effizienz zu verbessern, da der Zugriff auf den Arbeitsspeicher schreibgeschützt ist.

Weitere [](performance-optimizations.md) Informationen zur Verwendung \_ von D3DLOCK DISCARD oder D3DLOCK \_ noüberschreitungen für den flags-Parameter von [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)finden Sie unter Verwenden von dynamischen Scheitelpunkt-und Index Puffern.

Stellen Sie in C++ sicher, dass die Anwendung ordnungsgemäß auf den zugeordneten Speicher zugreift, da Sie direkt auf den für den Vertex-Puffer reservierten Arbeitsspeicher zugreifen. Andernfalls riskieren Sie, dass der Arbeitsspeicher ungültig wird. Verwenden Sie den Schritt des Vertex-Formats, das Ihre Anwendung verwendet, um von einem Scheitelpunkt im zugewiesenen Puffer zu einem anderen zu wechseln. Der Vertex-Pufferspeicher ist ein einfaches Array von Vertices, das in "f" angegeben ist. Verwenden Sie den Schritt der von Ihnen definierten Scheitelpunkt Format Struktur. Sie können den Schritt jedes Scheitel Punkts zur Laufzeit berechnen, indem Sie die in der Vertex-Puffer Beschreibung enthaltene [D3DFVF](d3dfvf.md) untersuchen. In der folgenden Tabelle wird die Größe der einzelnen Scheitelpunkt Komponenten angezeigt.



| Vertex-formatflag | Size              |
|--------------------|-------------------|
| D3DFVF \_ diffuses    | sizeof (DWORD)     |
| D3DFVF \_ Normal     | sizeof (float) x 3 |
| D3DFVF \_ Glanz   | sizeof (DWORD)     |
| D3DFVF \_ texn       | sizeof (float) x n |
| D3DFVF \_ XYZ        | sizeof (float) x 3 |
| D3DFVF \_ xyzrhw     | sizeof (float) x 4 |



 

Die Anzahl der im Vertex-Format vorhandenen Texturkoordinaten wird durch die D3DFVF \_ tex n-Flags beschrieben (wobei n für einen Wert zwischen 0 und 8 steht). Multiplizieren Sie die Anzahl der Texturkoordinaten Sätze um die Größe eines Satzes von Texturkoordinaten, der von einem bis vier Gleit Komma Zahlen reichen kann, um den für diese Anzahl von Texturkoordinaten erforderlichen Arbeitsspeicher zu berechnen.

Verwenden Sie den gesamten vertexstride, um den Speicher Zeiger nach Bedarf zu erhöhen und zu verringern, um auf bestimmte Scheitel Punkte zuzugreifen.

## <a name="retrieving-vertex-buffer-descriptions"></a>Abrufen von Vertex-Puffer Beschreibungen

Sie können Informationen zu einem Vertex-Puffer abrufen, indem Sie die [**IDirect3DVertexBuffer9:: getdesc**](/windows/desktop/api) -Methode aufrufen. Diese Methode füllt die Member der [**D3DVERTEXBUFFER \_ DESC**](d3dvertexbuffer-desc.md) -Struktur mit Informationen über den Scheitelpunkt Puffer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Puffer](vertex-buffers.md)
</dt> </dl>

 

 
