---
description: Eine Kombination von 0 (null) oder mehreren Sperr Optionen, die den Typ der auszuführenden Sperre beschreiben.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3a60318aad8ae0fadcf02d5dea76f6aa62548
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748729"
---
# <a name="d3dlock"></a>D3DLOCK

Eine Kombination von 0 (null) oder mehreren Sperr Optionen, die den Typ der auszuführenden Sperre beschreiben.



|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definieren                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| D3DLOCK \_ verwerfen           | Die Anwendung verwirft den gesamten Arbeitsspeicher innerhalb der gesperrten Region. Für Scheitelpunkt-und Index Puffer wird der gesamte Puffer verworfen. Diese Option ist nur gültig, wenn die Ressource mit dynamischer Verwendung erstellt wird (siehe [D3DUSAGE](d3dusage.md)).                                                                                                                                                                                                                                                                                                                                                           |
| D3DLOCK \_ donotwait         | Ermöglicht es einer Anwendung, CPU-Zyklen zurückzugewinnen, wenn der Treiber die-Oberfläche nicht sofort sperren kann. Wenn dieses Flag festgelegt ist und der Treiber die-Oberfläche nicht sofort sperren kann, gibt der Lock-Befehl D3DERR \_ wasstilldrawing zurück. Dieses Flag kann nur verwendet werden, wenn eine Oberfläche gesperrt wird, die mithilfe von "| [**ateoffscreenplainsurface**](/windows/desktop/api)", " [**kreaterendertarget**](/windows/desktop/api)" oder " [**kreatedepthschablone**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)" erstellt wurde. Dieses Flag kann auch mit einem Hintergrund Puffer verwendet werden.            |
| D3DLOCK \_ kein \_ Dirty \_ Update | Standardmäßig fügt eine Sperre für eine Ressource der Ressource einen geänderten Bereich hinzu. Diese Option verhindert Änderungen am geänderten Zustand der Ressource. Anwendungen sollten diese Option verwenden, wenn Sie über zusätzliche Informationen über den Satz von Regionen verfügen, der während des Sperr Vorgangs geändert wurde.                                                                                                                                                                                                                                                                                                                    |
| D3DLOCK \_ noüberschreibung       | Gibt an, dass der Arbeitsspeicher, auf den in einem Zeichnungs aufrufzeichen seit der letzten Sperre ohne dieses Flag verwiesen wurde, während der Sperre nicht geändert wird. Dadurch können Optimierungen aktiviert werden, wenn die Anwendung Daten an eine Ressource anfügt. Wenn Sie dieses Flag angeben, kann der Treiber sofort zurückkehren, wenn die Ressource verwendet wird. andernfalls muss der Treiber die Verwendung der Ressource beenden, bevor die Sperre zurückgegeben wird.                                                                                                                                                                                            |
| D3DLOCK \_ nosyslock         | Das Standardverhalten einer Videospeicher Sperre besteht darin, einen systemweiten kritischen Abschnitt zu reservieren. Dadurch wird sichergestellt, dass für die Dauer der Sperre keine Änderungen des Anzeigemodus auftreten. Diese Option bewirkt, dass der systemweite kritische Abschnitt für die Dauer der Sperre nicht aufrechterhalten wird.<br/> Der Sperr Vorgang ist zeitaufwändig, kann jedoch dem System ermöglichen, andere Aufgaben auszuführen, z. b. das Bewegen des Mauszeigers. Diese Option ist für Sperren mit langer Dauer nützlich, wie z. b. die Sperre des Hintergrund Puffers für das Software Rendering, das sich andernfalls nachteilig auf die Reaktionsfähigkeit des Systems auswirkt.<br/> |
| D3DLOCK \_ schreibgeschützt          | Die Anwendung schreibt nicht in den Puffer. Dadurch können Ressourcen, die in nicht nativen Formaten gespeichert sind, beim Entsperren den Schritt zum erneuten komprimieren speichern.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a>Konstante Informationen



|                          |             |
|--------------------------|-------------|
| Header                   | d3d9types. h |
| Mindestens Betriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**Lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Sperre**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**Lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Sperre**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**Lockbox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**Lockbox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[**Lockvertexbuffer**](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

**Lockvertexbuffer**
</dt> <dt>

[**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[**Lockvertexbuffer**](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
