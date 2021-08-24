---
description: Bei der Texturverwaltung wird bestimmt, welche Texturen zum Rendern zu einem bestimmten Zeitpunkt benötigt werden, und es wird sichergestellt, dass diese Texturen in den Videospeicher geladen werden.
ms.assetid: ea6d64ee-f570-49eb-b5fd-67fcde3f8ddc
title: Automatische Texturverwaltung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c65168947acb05c8437836ba0b27765a9b03d3ba97fd223f50eb9a99ab8c50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751400"
---
# <a name="automatic-texture-management-direct3d-9"></a>Automatische Texturverwaltung (Direct3D 9)

Bei der Texturverwaltung wird bestimmt, welche Texturen zum Rendern zu einem bestimmten Zeitpunkt benötigt werden, und es wird sichergestellt, dass diese Texturen in den Videospeicher geladen werden. Wie bei jedem Algorithmus variieren Texturverwaltungsschemas in ihrer Komplexität, aber jeder Ansatz für die Texturverwaltung umfasst die folgenden wichtigen Aufgaben.

-   Nachverfolgen der Menge des verfügbaren Texturspeichers.
-   Berechnen, welche Texturen für das Rendering benötigt werden und welche nicht.
-   Bestimmen, welche vorhandenen Texturressourcen mit einem anderen Texturbild erneut geladen werden können und welche Oberflächen zerstört und durch neue Texturressourcen ersetzt werden sollen.

Direct3D implementiert die systemgestützte Texturverwaltung, um sicherzustellen, dass Texturen geladen werden, um eine optimale Leistung zu erzielen. Texturressourcen, die von Direct3D verwaltet werden, werden als verwaltete Texturen bezeichnet.

Der Textur-Manager verfolgt Texturen mit einem Zeitstempel nach, der identifiziert, wann die Textur zuletzt verwendet wurde. Anschließend wird ein algorithmus verwendet, der am wenigsten zuletzt verwendet wird, um zu bestimmen, welche Texturen entfernt werden sollen. Texturprioritäten werden als Tiebreaker verwendet, wenn zwei Texturen aus dem Arbeitsspeicher entfernt werden sollen. Wenn zwei Texturen denselben Prioritätswert aufweisen, wird die zuletzt verwendete Textur entfernt. Wenn jedoch zwei Texturen denselben Zeitstempel aufweisen, wird zuerst die Textur mit einer niedrigeren Priorität entfernt.

Sie fordern die automatische Texturverwaltung für Texturoberflächen an, wenn Sie sie erstellen. Um eine verwaltete Textur in einer C++-Anwendung abzurufen, erstellen Sie eine Texturressource, indem Sie [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) aufrufen und D3DPOOL MANAGED für den \_ Pool-Parameter angeben. Sie können nicht angeben, wo die Textur erstellt werden soll. Sie können die D3DPOOL DEFAULT- oder \_ D3DPOOL \_ SYSTEMMEM-Flags nicht verwenden, wenn Sie eine verwaltete Textur erstellen. Nach dem Erstellen der verwalteten Textur können Sie die [**IDirect3DDevice9::SetTexture-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) aufrufen, um sie auf eine Stufe in der Texturkaskaskade des Renderinggeräts zu setzen.

Sie können verwalteten Texturen eine Priorität zuweisen, indem Sie die [**IDirect3DResource9::SetPriority-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) für die Texturoberfläche aufrufen.

Direct3D lädt Texturen bei Bedarf automatisch in den Videospeicher herunter. Abhängig von der Verfügbarkeit des nicht lokalen Videospeichers oder anderer Faktoren kann das System verwaltete Texturen im lokalen oder nicht lokalen Videospeicher zwischenspeichern. Der Cachespeicherort Ihrer verwalteten Texturen wird nicht an Ihre Anwendung übermittelt, und diese Informationen sind auch nicht erforderlich, um die automatische Texturverwaltung zu verwenden. Wenn Ihre Anwendung mehr Texturen verwendet, als in den Videospeicher passen, entfernt Direct3D ältere Texturen aus dem Videospeicher, um Platz für die neuen Texturen zu machen. Wenn Sie erneut eine entfernte Textur verwenden, verwendet das System die ursprüngliche Systemspeichertexturoberfläche, um die Textur erneut in den Videospeichercache zu laden. Obwohl das erneute Laden der Textur erforderlich ist, verringert es auch die Leistung der Anwendung.

Sie können die ursprüngliche Systemspeicherkopie der Textur dynamisch ändern, indem Sie die Texturressource aktualisieren oder sperren. Wenn das System eine geänderte Oberfläche erkennt – nach Abschluss eines Updates oder wenn die Oberfläche entsperrt ist – aktualisiert der Textur-Manager automatisch die Videospeicherkopie der Textur. Die verursachten Leistungstreffer ähneln dem erneuten Laden einer entfernten Textur.

Wenn Sie in einem Spiel eine neue Ebene eingeben, muss Ihre Anwendung möglicherweise alle verwalteten Texturen aus dem Videospeicher leeren (durch Aufrufen von [**IDirect3DDevice9::EvictManagedResources**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-evictmanagedresources)).

Weitere Informationen zur Ressourcenverwaltung finden Sie unter [Verwalten von Ressourcen (Direct3D 9).](managing-resources.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
