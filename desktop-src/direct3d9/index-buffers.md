---
description: Index Puffer, die von der IDirect3DIndexBuffer9-Schnittstelle dargestellt werden, sind Speicherpuffer, die Indexdaten enthalten.
ms.assetid: baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784
title: Index Puffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7151fae6deb72a0c569d269c80e5b13bf946f9d0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860090"
---
# <a name="index-buffers-direct3d-9"></a>Index Puffer (Direct3D 9)

Index Puffer, die von der [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) -Schnittstelle dargestellt werden, sind Speicherpuffer, die Indexdaten enthalten. Index Daten (Indizes) sind ganzzahlige Offsets in Scheitelpunkt Puffer und werden zum Rendering primitiver mithilfe der [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) -Methode verwendet.

Ein Scheitelpunkt Puffer enthält Scheitel Punkte. Daher können Sie einen Scheitelpunkt Puffer entweder mit oder ohne indizierte primitive zeichnen. Da ein Index Puffer jedoch Indizes enthält, kann kein Index Puffer ohne entsprechenden Scheitelpunkt Puffer verwendet werden. (Als neben Hinweis [**IDirect3DDevice9::D rawindexedprimitiveup**](/windows/desktop/api) und [**IDirect3DDevice9::D rawprimitiveup**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup) sind die einzigen Draw-Methoden, die ohne Index oder Scheitelpunkt Puffer gezeichnet werden.)

## <a name="index-buffer-description"></a>Beschreibung des Index Puffers

Ein Index Puffer wird in Bezug auf seine Funktionen beschrieben, z. b. wo er im Arbeitsspeicher vorhanden ist, ob er Lese-und Schreibvorgänge unterstützt und wie der Typ und die Anzahl der Indizes enthalten sein können. Diese Merkmale werden in einer [**D3DINDEXBUFFER- \_**](d3dindexbuffer-desc.md) Debug-Struktur gespeichert.

Index Puffer Beschreibungen Teilen der Anwendung mit, wie ein vorhandener Puffer erstellt wurde. Sie stellen eine leere Beschreibungs Struktur bereit, damit das System mit den Funktionen eines zuvor erstellten Index Puffers aufgefüllt werden soll.

-   Der formatmember beschreibt das Oberflächen Format der Index Puffer Daten.
-   Der Typ identifiziert den Ressourcentyp des Index Puffers.
-   Der Member der Verwendungs Struktur enthält allgemeine funktionsflags. Das D3DUSAGE \_ softwareprocessing-Flag gibt an, dass der Index Puffer bei der Verarbeitung von Software Scheitel Punkten verwendet werden soll. Das vorhanden sein des Kennzeichens D3DUSAGE \_ Schreibweise in der Verwendung gibt an, dass der Speicher des Index Puffers nur für Schreibvorgänge verwendet wird. Dadurch wird der Treiber freigegeben, um die Indexdaten am besten Speicherort zu platzieren, um schnelle Verarbeitung und Rendering zu ermöglichen. Wenn das \_ Flag D3DUSAGE Write only nicht verwendet wird, ist es weniger wahrscheinlich, dass der Treiber die Daten an einem Speicherort speichert, der für Lesevorgänge ineffizient ist. Dadurch wird die Verarbeitungs-und renderinggeschwindigkeit verringert. Wenn dieses Flag nicht angegeben wird, wird davon ausgegangen, dass Anwendungen Lese-und Schreibvorgänge für die Daten im Index Puffer ausführen.
-   Pool gibt die Speicher Klasse an, die dem Index Puffer zugeordnet ist. Das D3DPOOL \_ SystemMem-Flag gibt an, dass das System den Index Puffer im Systemspeicher erstellt hat.
-   Der Size-Member speichert die Größe der Vertex-Puffer Daten in Bytes.
-   Der letzte Parameter "psharedhandle" wird nicht verwendet. Legen Sie den Wert auf **null** fest.

## <a name="index-processing-requirements"></a>Anforderungen an die Index Verarbeitung

Die Leistung von Index Verarbeitungsvorgängen hängt stark davon ab, wo der Index Puffer im Arbeitsspeicher vorhanden ist und welche Art von renderinggerät verwendet wird. Anwendungen steuern die Speicher Belegung für Index Puffer, wenn Sie erstellt werden. Wenn das D3DPOOL \_ SystemMem-Speicherflag festgelegt ist, wird der Index Puffer im Systemspeicher erstellt. Wenn das D3DPOOL- \_ standardarbeitsspeicherflag verwendet wird, bestimmt der Gerätetreiber, wo der Speicher für den Index Puffer am besten zugewiesen wird. Dies wird häufig als Treiber optimaler Arbeitsspeicher bezeichnet. Treiber-optimaler Arbeitsspeicher kann lokaler Videospeicher, nicht lokaler Videospeicher oder System Arbeitsspeicher sein.

Wenn das D3DUSAGE \_ softwareprocessing-verhaltenflag beim Aufrufen der Methode [**IDirect3DDevice9:: createindexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) festgelegt wird, wird angegeben, dass der Index Puffer bei der Verarbeitung von Software Scheitel Punkten verwendet werden soll. Dieses Flag ist für die Vertexverarbeitung im gemischten Modus erforderlich (D3DCREATE \_ mixed \_ vertexprocessing), wenn die Verarbeitung von Software Scheitel Punkten verwendet wird.

Die Anwendung kann Indizes direkt in einen Index Puffer schreiben, der im Treiber optimalen Arbeitsspeicher zugeordnet ist. Dieses Verfahren verhindert einen redundanten Kopiervorgang zu einem späteren Zeitpunkt. Diese Technik funktioniert nicht gut, wenn Ihre Anwendung Daten aus einem Index Puffer liest, da Lesevorgänge, die vom Host aus dem Treiber optimalen Arbeitsspeicher durchgeführt werden, sehr langsam sein können. Wenn Ihre Anwendung während der Verarbeitung lesen oder Daten in den Puffer schreiben muss, ist ein Index Puffer für den System Arbeitsspeicher daher eine bessere Wahl.

> [!Note]  
> Verwenden Sie immer D3DPOOL \_ Default, es sei denn, Sie möchten keinen Videospeicher verwenden oder große Mengen von Seiten gesperrtem RAM verwenden, wenn der Treiber den Scheitelpunkt-oder Index Puffer in den AGP-Speicher versetzt.

 

## <a name="create-an-index-buffer"></a>Erstellen eines Index Puffers

Erstellen Sie ein Index Puffer Objekt, indem Sie die [**IDirect3DDevice9:: createindexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) -Methode aufrufen, die sechs Parameter akzeptiert.

-   Der erste Parameter gibt die Länge des Index Puffers in Bytes an.
-   Der zweite Parameter ist ein Satz von Verwendungs Steuerelementen. Der Wert bestimmt unter anderem, ob die Scheitel Punkte, auf die die Indizes verweisen, clippinginformationen enthalten können. Um die Leistung zu verbessern, geben Sie D3DUSAGE \_ DoNotClip an, wenn Clipping nicht erforderlich ist.

    Das D3DUSAGE \_ softwareprocessing-Flag kann festgelegt werden, wenn der gemischte Modus oder die Verarbeitung von Software Scheitel Punkten (D3DCREATE \_ mixed \_ vertexprocessing/D3DCREATE \_ Software \_ vertexprocessing) für dieses Gerät aktiviert ist. D3DUSAGE \_ softwareprocessing muss für Puffer festgelegt werden, die bei der Verarbeitung von Software Scheitel Punkten im gemischten Modus verwendet werden. für die bestmögliche Leistung sollte jedoch bei Verwendung der Hardware Index Verarbeitung im gemischten Modus (D3DCREATE \_ Hardware \_ vertexprocessing) nicht festgelegt werden. Das Festlegen von D3DUSAGE \_ softwareprocessing ist jedoch die einzige Option, wenn ein einzelner Puffer sowohl bei der Hardware-als auch bei der Verarbeitung von Software Scheitel Punkten verwendet wird. D3DUSAGE \_ softwareprocessing ist für gemischte und Software Geräte zulässig.

    Es ist möglich, Vertex-und Index Puffer in den Systemspeicher zu erzwingen, indem Sie D3DPOOL \_ SystemMem angeben, auch wenn die Index Verarbeitung in der Hardware erfolgt. Dies ist eine Möglichkeit, eine übermäßig große Menge an Seiten gesperrtem Arbeitsspeicher zu vermeiden, wenn ein Treiber diese Puffer in den AGP-Speicher versetzt.

-   Der dritte Parameter ist entweder der D3DFMT \_ INDEX16-Member oder der D3DFMT \_ INDEX32-Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der die Größe jedes Indexes angibt.

-   Der vierte Parameter ist ein Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der dem System mitteilt, wo im Arbeitsspeicher der neue Index Puffer platziert werden soll.

-   Der letzte Parameter, den [**IDirect3DDevice9:: anateindexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) annimmt, ist die Adresse einer Variablen, die mit einem Zeiger auf die neue [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) -Schnittstelle des Vertex-Puffer Objekts gefüllt ist, wenn der-Befehl erfolgreich ausgeführt wird.

Im folgenden C++-Codebeispiel wird gezeigt, wie das Erstellen eines Index Puffers im Code aussehen könnte.


```
/*
 * For the purposes of this example, the d3dDevice variable is the 
 * address of an IDirect3DDevice9 interface exposed by a 
 * Direct3DDevice object, g_IB is a variable of type 
 * LPDIRECT3DINDEXBUFFER9.
 */

if( FAILED( d3dDevice->CreateIndexBuffer( 16384 *sizeof(WORD),
           D3DUSAGE_WRITEONLY, D3DFMT_INDEX16, D3DPOOL_DEFAULT, 
           &g_IB, NULL ) ) )
    return E_FAIL;
```



## <a name="access-an-index-buffer"></a>Zugreifen auf einen Index Puffer

Index Puffer Objekte ermöglichen Anwendungen den direkten Zugriff auf den für Indexdaten zugewiesenen Arbeitsspeicher. Sie können einen Zeiger auf den Speicher des Index Puffers abrufen, indem Sie die [**IDirect3DIndexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) -Methode aufrufen und dann nach Bedarf auf den Speicher zugreifen, um den Puffer mit neuen Indexdaten auszufüllen oder darin enthaltene Daten zu lesen. Die Lock-Methode akzeptiert vier Parameter. Der erste, *offsetToLock*, ist der Offset in die Indexdaten. Der zweite Parameter ist die Größe der Indexdaten (in Byte gemessen). Der dritte Parameter, der von der **IDirect3DIndexBuffer9:: Lock** -Methode, *ppbdata*, akzeptiert wird, ist die Adresse eines Byte Zeigers, der mit einem Zeiger auf die Indexdaten gefüllt wird, wenn der-Befehl erfolgreich ausgeführt wird.

Der letzte Parameter, *Flags*, teilt dem System mit, wie der Arbeitsspeicher gesperrt werden soll. Sie können es verwenden, um anzugeben, wie die Anwendung auf die Daten im Puffer zugreift. Geben Sie Konstanten für den *Flags* -Parameter entsprechend der Art und Weise an, wie von Ihrer Anwendung auf die Indexdaten zugegriffen wird. Dies ermöglicht es dem Treiber, den Arbeitsspeicher zu sperren und die bestmögliche Leistung für den angeforderten Zugriffstyp bereitzustellen. Verwenden Sie das D3DLOCK-Flag "schreibgeschützt", \_ Wenn die Anwendung nur aus dem Speicher des Index Puffers liest. Das Einschließen dieses Flags ermöglicht Direct3D, seine internen Prozeduren zu optimieren, um die Effizienz zu verbessern, da der Zugriff auf den Arbeitsspeicher schreibgeschützt ist.

Nachdem Sie die Indexdaten ausgefüllt oder gelesen haben, nennen Sie die [**IDirect3DIndexBuffer9:: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-unlock) -Methode, wie im folgenden Codebeispiel gezeigt.


```
// This code example assumes the m_pIndexBuffer is a variable of type 
// LPDIRECT3DINDEXBUFFER9 and that g_Indices has been properly 
// initialized with indices.

// To fill the index buffer, you must lock the buffer to gain 
// access to the indices. This mechanism is required because index
// buffers may be in device memory.

VOID* pIndices;

if( FAILED( m_pIndexBuffer->Lock( 
      0,                 // Fill from start of the buffer
      sizeof(g_Indices), // Size of the data to load
      BYTE**)&pIndices,  // Returned index data
      0 ) ) )            // Send default flags to the lock
{
    SAFE_RELEASE(m_pIndexBuffer);
    return E_FAIL;
}

memcpy( pIndices, g_Indices, sizeof(g_Indices) );
m_pIndexBuffer->Unlock();
```



> [!Note]
>
> Wenn Sie einen Index Puffer mit dem Flag "D3DUSAGE \_ schreibonly" erstellen, verwenden Sie das Sperr Kennzeichen "D3DLOCK Read only" nicht \_ . Verwenden Sie das D3DLOCK-Flag "schreibgeschützt", \_ Wenn die Anwendung nur aus dem Speicher des Index Puffers liest. Das Einschließen dieses Flags ermöglicht Direct3D, seine internen Prozeduren zu optimieren, um die Effizienz zu verbessern, da der Zugriff auf den Arbeitsspeicher schreibgeschützt ist.
>
> Weitere Informationen zur Verwendung \_ von D3DLOCK DISCARD oder D3DLOCK \_ noüberschreitungen für den *Flags* -Parameter der [**IDirect3DIndexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) -Methode finden Sie unter [Leistungsoptimierungen (Direct3D 9)](performance-optimizations.md).

 

Stellen Sie in C++ sicher, dass die Anwendung ordnungsgemäß auf den zugeordneten Arbeitsspeicher zugreift, da Sie direkt auf den für den Index Puffer reservierten Arbeitsspeicher zugreifen. Andernfalls riskieren Sie, dass der Arbeitsspeicher ungültig wird. Verwenden Sie den Schritt des Index Formats, das Ihre Anwendung verwendet, um von einem Index im zugeordneten Puffer zu einem anderen zu wechseln.

Rufen Sie Informationen zu einem Index Puffer ab, indem Sie die [**IDirect3DIndexBuffer9:: getdesc**](/windows/desktop/api) -Methode aufrufen. Diese Methode füllt die Member der [**D3DINDEXBUFFER \_ DESC**](d3dindexbuffer-desc.md) -Struktur mit Informationen über den Index Puffer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Ressourcen](direct3d-resources.md)
</dt> <dt>

[Rendering aus Scheitelpunkt-und Index Puffer (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Vertex-Puffer (Direct3D 9)](vertex-buffers.md)
</dt> </dl>

 

 
