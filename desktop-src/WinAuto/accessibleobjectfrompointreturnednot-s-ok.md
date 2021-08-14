---
title: AccessibleObjectFromPointReturnedNot_S_OK
description: AccessibleObjectFromPointReturnedNot \_ S \_ OK
ms.assetid: F5DA071A-EBB8-454C-9BC0-BC798835B7D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ceabd15e5a401bb67ac14af5a7fb83b96543b4b8046ceee2349d8d57b8de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327686"
---
# <a name="accessibleobjectfrompointreturnednot_s_ok"></a>AccessibleObjectFromPointReturnedNot \_ S \_ OK

## <a name="text"></a>Text

AccessibleObjectFromPoint( {0} , ) hat zurückgegeben und erwartet S {1} {2} \_ OK

## <a name="type"></a>type

Warnung

## <a name="description"></a>BESCHREIBUNG

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) hat S OK nicht \_ wie erwartet für die angegebenen Koordinaten zurückgeben.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Die Benutzerinteraktion während der Überprüfung, z. B. das Verschieben des Fokus auf ein HWND ohne Ziel, beeinträchtigt den Überprüfungsprozess.
-   Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Navigation durch Treffertests und Bildschirmposition](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




