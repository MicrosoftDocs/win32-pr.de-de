---
description: Eine Kombination aus 0 (null) oder mehr Sperroptionen, die den Typ der durchzuführenden Sperre beschreiben.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adaeddbc1aff0812d3e0f67df90c2cf9b1118347
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999427"
---
# <a name="d3dlock"></a>D3DLOCK

Eine Kombination aus 0 (null) oder mehr Sperroptionen, die den Typ der durchzuführenden Sperre beschreiben.



| \#Definieren                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DLOCK \_ DISCARD           | Die Anwendung verwirft den ganzen Arbeitsspeicher im gesperrten Bereich. Für Scheitelpunkt- und Indexpuffer wird der gesamte Puffer verworfen. Diese Option ist nur gültig, wenn die Ressource mit dynamischer Nutzung erstellt wird (siehe [D3DUSAGE](d3dusage.md)).                                                                                                                                                                                                                                                                                                                                                           |
| D3DLOCK \_ DONOTWAIT         | Ermöglicht es einer Anwendung, CPU-Zyklen zurück zu erhalten, wenn der Treiber die Oberfläche nicht sofort sperren kann. Wenn dieses Flag festgelegt ist und der Treiber die Oberfläche nicht sofort sperren kann, gibt der Sperraufruf D3DERR \_ WASAUFRUFDRAWING zurück. Dieses Flag kann nur verwendet werden, wenn eine Oberfläche gesperrt wird, die mit [**CreateOffscreenPlainSurface,**](/windows/desktop/api) [**CreateRenderTarget**](/windows/desktop/api)oder [**CreateDepthStencilSurface erstellt wurde.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) Dieses Flag kann auch mit einem Hintergrundpuffer verwendet werden.            |
| D3DLOCK \_ KEIN \_ GEÄNDERTES \_ UPDATE | Standardmäßig fügt eine Sperre für eine Ressource dieser Ressource eine verfeinerte Region hinzu. Diese Option verhindert Änderungen am geänderten Zustand der Ressource. Anwendungen sollten diese Option verwenden, wenn sie über zusätzliche Informationen über den Satz von Regionen verfügen, die während des Sperrvorganges geändert wurden.                                                                                                                                                                                                                                                                                                                    |
| D3DLOCK \_ NOOVERWRITE       | Gibt an, dass der Arbeitsspeicher, auf den seit der letzten Sperre ohne dieses Flag in einem Zeichnungsaufruf verwiesen wurde, während der Sperre nicht geändert wird. Dies kann Optimierungen ermöglichen, wenn die Anwendung Daten an eine Ressource anfügt. Durch Die Angabe dieses Flags kann der Treiber sofort zurückkehren, wenn die Ressource verwendet wird. Andernfalls muss der Treiber die Verwendung der Ressource beenden, bevor die Sperrung aufgehoben wird.                                                                                                                                                                                            |
| D3DLOCK \_ NOSYSLOCK         | Das Standardverhalten einer Videospeichersperre besteht darin, einen systemweiten kritischen Abschnitt zu reservieren, wodurch sichergestellt wird, dass für die Dauer der Sperre keine Änderungen am Anzeigemodus vorgenommen werden. Diese Option bewirkt, dass der systemweite kritische Abschnitt für die Dauer der Sperre nicht gehalten wird.<br/> Der Sperrvorgang ist zeitaufwändig, kann es dem System jedoch ermöglichen, andere Aufgaben auszuführen, z. B. das Bewegen des Mauszeigers. Diese Option ist nützlich für Sperren mit langer Dauer, z. B. die Sperre des Hintergrundpuffers für das Softwarerendering, die andernfalls die Reaktionsfähigkeit des Systems beeinträchtigen würde.<br/> |
| D3DLOCK \_ READONLY          | Die Anwendung schreibt nicht in den Puffer. Dadurch können Ressourcen, die in nicht nativen Formaten gespeichert sind, beim Entsperren den Schritt zur Erneutkomprimierung speichern.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a>Konstanteninformationen



|                          |             |
|--------------------------|-------------|
| Header                   | d3d9types.h |
| Mindestbetriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Sperre**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Sperre**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**Lockbox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**Lockbox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[**LockVertexBuffer**](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

**LockVertexBuffer**
</dt> <dt>

[**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
