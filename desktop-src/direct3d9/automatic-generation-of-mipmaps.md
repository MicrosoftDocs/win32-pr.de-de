---
description: Sie können jetzt automatisch eine MipMap erstellen, bei der es sich um eine Reihe von Texturen handelt, die jeweils nach einer anderen Auflösung gefiltert werden.
ms.assetid: ae5955f9-e52a-41d7-a199-800e37a3e936
title: Automatische Generierung von Mipmaps (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fda5b765d42ffa10f8cc5998daa66ae36c2bc75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346446"
---
# <a name="automatic-generation-of-mipmaps-direct3d-9"></a>Automatische Generierung von Mipmaps (Direct3D 9)

Sie können jetzt automatisch eine MipMap erstellen, bei der es sich um eine Reihe von Texturen handelt, die jeweils nach einer anderen Auflösung gefiltert werden. Mipmaps werden häufig verwendet, um beim Rendern verschiedene Detailebenen bereitzustellen. Das automatische Erstellen von Mipmaps zum Zeitpunkt der Textur Erstellung nutzt die Hardware Filterung, da sich die MipMap im Videospeicher befindet.

Um eine MipMap automatisch zu generieren, legen Sie vor dem Aufrufen von [**CreateTexture**](/windows/desktop/api)eine neue Verwendung [D3DUSAGE \_ autogenmipmap](d3dusage.md) fest. Die untergeordnete Generierung von diesem Punkt auf ist für die Anwendung vollständig transparent. Nur die obere Textur Ebene ist für die Anwendung zugänglich. der Zugriff auf die Textur Unterebenen ist nicht möglich, da Sie nur erstellt werden, wenn Sie vom Treiber benötigt werden. In Fällen, in denen die Generierung der untergeordneten Ebene viel Zeit in Anspruch nehmen kann, verwenden Sie [**generatemipsublevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) , um dem Treiber zu entnehmen, dass er untergeordnete Ebenen für die jeweilige Anwendung generieren soll.

## <a name="mipmap-filtering"></a>Filterung von MipMap

Der " [**abtauthgenfiltertype**](/windows/desktop/api) " steuert die Filterqualität während der automatischen Generierung. Wenn Sie den Filtertyp ändern, werden die MipMap-Unterebenen und bewirkt, dass Sie neu generiert werden. Verwenden Sie [**getautogenfiltertype**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getautogenfiltertype) , um den aktuellen Filtertyp zu erhalten. Der Standard Filtertyp ist D3DTEXF \_ linear. Wenn der Treiber keinen linearen Filter unterstützt, wird der Filtertyp auf D3DTEXF Point festgelegt \_ .

Diese Methoden haben keine Auswirkung, wenn die Textur nicht mit [D3DUSAGE \_ autogenmipmap](d3dusage.md) erstellt wird und kein Fehler zurückgegeben wird. Alle Filtertypen, die vom Treiber für die reguläre Textur Filterung unterstützt werden, werden automatisch generiert, ausgenommen D3DTEXF \_ None. Für jeden Ressourcentyp sollten die Treiber alle Filtertypen unterstützen, die in den entsprechenden Textur-, cubetexture-und volumetexture-Filter Caps gemeldet werden.

Wenn Sie überprüfen möchten, welche Filtertypen unterstützt werden, überprüfen Sie, welche Caps von den TextureFilterCaps-und/oder cubetexturefiltercaps-Membern von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)unterstützt werden.

## <a name="mipmap-support"></a>MipMap-Unterstützung

[D3DUSAGE \_ Autogenmipmap](d3dusage.md) ist nur ein Hinweis, und diese Angabe während der Textur Erstellung oder beim Aufrufen von [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) verursacht keinen Fehler für einen der DDI-Typen (Device Driver Interface).

Das Aufrufen von [**UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) ist unzulässig, wenn die Quelle eine automatisch generierte MipMap ist, das Ziel jedoch nicht. Die Quelle kann eine nicht automatisch generierte MipMap sein, und das Ziel kann eine automatisch generierte MipMap sein. In diesem Fall wird nur die oberste übereinstimmende Ebene aktualisiert. Alle anderen Quell Unterebenen werden ignoriert. Wenn sowohl Quelle als auch Ziel automatisch generiert werden, wird auf ähnliche Weise nur die oberste übereinstimmende Ebene aktualisiert. Die untergeordneten Ebenen der Quelle werden ignoriert, und die Ziel Unterebenen werden neu generiert.

Um die Unterstützung für die automatische Generierung von Mipmaps zu überprüfen, prüfen Sie, ob [D3DCAPS2 \_ canautogenmipmap](d3dcaps2.md) festgelegt ist. Wenn dies der Fall ist, wenden Sie [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit [D3DUSAGE \_ autogenmipmap](d3dusage.md)an. Wenn der Rückgabewert D3D \_ OK ist, wird sichergestellt, dass die Mipmaps automatisch generiert werden. Wenn der Rückgabewert D3DOK \_ noautogen ist, bedeutet dies, dass der Erstellungs Vorgang erfolgreich ist, es werden jedoch keine Mipmaps generiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
