---
description: Ein eingebettetes Objekt ist ein Objekt einer Klasse, das in einer Klassen-oder Instanzdeklaration einer anderen Klasse vorhanden ist.
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: Einbetten von Objekten in eine Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362853"
---
# <a name="embedding-objects-in-a-class"></a>Einbetten von Objekten in eine Klasse

Ein eingebettetes Objekt ist ein Objekt einer Klasse, das in einer Klassen-oder Instanzdeklaration einer anderen Klasse vorhanden ist. Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse enthält z. b. Win32-Vertrauens nehmer eingebettete Objekte. [**\_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) Jedes der **Win32- \_ Treuhänder** -Objekte enthält ein [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Objekt. Die Tiefe, in der eine Klasse über eingebettete Objekte verfügen kann, wird von WMI nicht eingeschränkt. Die Verwendung eines anderen Entwurfs, z. b. das Erstellen einer Zuordnungs Klasse, kann jedoch zu einem besser verwaltbaren Schema führen.

Weitere Informationen zu eingebetteten Objekten finden Sie in den folgenden Themen:

-   [Erstellen von eingebetteten Objekten](creating-embedded-objects.md)
-   [Abfragen von eingebetteten Objekten](querying-embedded-objects.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
