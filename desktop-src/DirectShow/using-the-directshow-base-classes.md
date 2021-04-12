---
description: Verwenden der DirectShow-Basisklassen
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: Verwenden der DirectShow-Basisklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216783"
---
# <a name="using-the-directshow-base-classes"></a>Verwenden der DirectShow-Basisklassen

Wenn Sie die Basisklassen in DirectShow verwenden möchten, müssen Sie die Basisklassen Bibliothek erstellen und verknüpfen.

Die Basisklassen Bibliothek wird als SDK-Beispiel im Microsoft Windows Software Development Kit (SDK) () bereitgestellt <https://go.microsoft.com/fwlink/p/?linkid=62332> . Der genaue Speicherort hängt von der Version des SDK ab, das Sie installiert haben, aber der relative Pfad lautet:

*(SDK Samples root)* \\ DirectShow- \\ baseclasses

Header: Streams. h

Library: das Beispiel erstellt die Verkaufs-und Debugversionen der Bibliothek:

-   Verkaufsversion: "mbase. lib"
-   Debugversion: "straumbasd. lib".

Weitere Informationen zum Einrichten der Buildumgebung finden Sie unter [Einrichten der Buildumgebung](setting-up-the-build-environment.md).

## <a name="preprocessor-symbols"></a>Präprozessorsymbole

Wenn Sie die Header Datei Streams. h einschließen, haben die folgenden Präprozessorsymbole eine besondere Bedeutung:

-   Perf: reserviert. Verwenden Sie dieses Präprozessorsymbol nicht.
-   Vfwrobust: aktiviert die Zeiger Validierung im Einzelhandel. Weitere Informationen finden Sie unter [Zeiger Validierungs Makros](pointer-validation-macros.md). In Debugbuilds ist es nicht notwendig, vfwrobust zu definieren.

> [!Note]  
> In Windows Vista und höher sind die Zeiger Validierungs Makros leer.

 

 

 



