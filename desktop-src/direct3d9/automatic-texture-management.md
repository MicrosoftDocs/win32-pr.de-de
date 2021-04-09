---
description: Bei der Textur Verwaltung wird festgelegt, welche Texturen zum Rendern zu einem bestimmten Zeitpunkt benötigt werden, und sicherstellen, dass diese Texturen in den Videospeicher geladen werden.
ms.assetid: ea6d64ee-f570-49eb-b5fd-67fcde3f8ddc
title: Automatische Textur Verwaltung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0eb14eede197661bc127a062229ebed31274ae8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861543"
---
# <a name="automatic-texture-management-direct3d-9"></a>Automatische Textur Verwaltung (Direct3D 9)

Bei der Textur Verwaltung wird festgelegt, welche Texturen zum Rendern zu einem bestimmten Zeitpunkt benötigt werden, und sicherstellen, dass diese Texturen in den Videospeicher geladen werden. Wie bei jedem beliebigen Algorithmus variieren Textur Verwaltungs Schemas in der Komplexität, aber jeder Ansatz für die Textur Verwaltung umfasst die folgenden wichtigen Aufgaben.

-   Die Menge des verfügbaren Textur Speichers wird nachverfolgt.
-   Berechnen, welche Texturen zum Rendern benötigt werden und welche nicht.
-   Bestimmen, welche vorhandenen Textur Ressourcen mit einem anderen Textur Bild neu geladen werden können, und welche Oberflächen zerstört und durch neue Textur Ressourcen ersetzt werden sollen.

Direct3D implementiert eine vom System unterstützte Textur Verwaltung, um sicherzustellen, dass Texturen für eine optimale Leistung geladen werden. Textur Ressourcen, die von Direct3D verwaltet werden, werden als verwaltete Texturen bezeichnet.

Der Textur-Manager verfolgt Texturen mit einem Zeitstempel, der angibt, wann die Textur zuletzt verwendet wurde. Anschließend wird mithilfe eines selten verwendeten Algorithmus festgelegt, welche Texturen entfernt werden sollen. Textur Prioritäten werden als Trennschalter verwendet, wenn zwei Texturen zum Entfernen aus dem Arbeitsspeicher verwendet werden. Wenn zwei Texturen denselben Prioritätswert aufweisen, wird die nicht zuletzt verwendete Textur entfernt. Wenn jedoch zwei Texturen denselben Zeitstempel aufweisen, wird die Textur mit niedrigerer Priorität zuerst entfernt.

Sie fordern bei der Erstellung eine automatische Textur Verwaltung für Textur Oberflächen an. Um eine verwaltete Textur in einer C++-Anwendung abzurufen, erstellen Sie eine Textur Ressource, indem Sie [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) aufrufen und die D3DPOOL angeben, die \_ für den Pool Parameter verwaltet werden. Sie dürfen nicht angeben, wo die Textur erstellt werden soll. \_Beim Erstellen einer verwalteten Textur können die D3DPOOL default-oder D3DPOOL SystemMem-Flags nicht verwendet werden \_ . Nachdem Sie die verwaltete Textur erstellt haben, können Sie die [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -Methode aufrufen, um Sie auf eine Stufe in der Textur Cascade des renderinggeräts festzulegen.

Sie können verwalteten Texturen eine Priorität zuweisen, indem Sie die [**IDirect3DResource9:: SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) -Methode für die Textur Oberfläche aufrufen.

Direct3D lädt Texturen nach Bedarf automatisch in den Videospeicher herunter. Das System kann verwaltete Texturen im lokalen oder nicht lokalen Videospeicher Zwischenspeichern, je nach Verfügbarkeit von nicht lokalem Videospeicher oder anderen Faktoren. Der Cache Speicherort Ihrer verwalteten Texturen wird nicht an die Anwendung übermittelt, und diese Informationen sind für die Verwendung der automatischen Textur Verwaltung nicht erforderlich. Wenn Ihre Anwendung mehr Texturen verwendet, als in den Videospeicher passen, entfernt Direct3D ältere Texturen aus dem Videospeicher, um Platz für die neuen Texturen zu schaffen. Wenn Sie eine entfernte Textur wieder verwenden, verwendet das System die ursprüngliche Textur Oberfläche des System Speichers, um die Textur im Video-Memory-Cache neu zu laden. Obwohl das erneute Laden der Textur notwendig ist, wird auch die Leistung der Anwendung verringert.

Sie können die ursprüngliche Systemspeicher Kopie der Textur dynamisch ändern, indem Sie die Textur Ressource aktualisieren oder sperren. Wenn das System eine modifizierte Oberfläche erkennt, nachdem ein Update abgeschlossen wurde, oder wenn die Oberfläche entsperrt ist, aktualisiert der Textur-Manager automatisch die Videospeicher Kopie der Textur. Der entstandene Leistungs Treffer ähnelt dem erneuten Laden einer entfernten Textur.

Wenn Sie eine neue Ebene in ein Spiel eingeben, muss Ihre Anwendung möglicherweise alle verwalteten Texturen aus dem Videospeicher leeren (durch Aufrufen von [**IDirect3DDevice9:: evictmanagedresources**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-evictmanagedresources)).

Weitere Informationen zur Ressourcenverwaltung finden Sie unter [Verwalten von Ressourcen (Direct3D 9)](managing-resources.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
