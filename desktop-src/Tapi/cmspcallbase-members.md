---
description: Die folgende Liste enthält die cmspcallbase-Member.
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: Cmspcallbase-Member
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216184"
---
# <a name="cmspcallbase-members"></a>Cmspcallbase-Member



| Memberart                   | Name             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                      | \*Mio. \_ pftm        | Zeiger auf den Free Threaded Marshaller.                                                                                                                                                                                                                                                                                                          |
| Cmspaddress\*                 | \*m \_ pmspaddress | Der Zeiger auf das MSP-Adress Objekt. Sie wird verwendet, um die Standard Terminals zu erhalten, wenn die Anwendung keine Auswahl spielt. Außerdem enthält es eine refcount (über [**mspaddressaddressf**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), nicht adressf), sodass die aggregierte Adresse nicht entfernt wird, während der Aufruf noch aktiv ist, aber die Adresse von TAPI 3 nicht adressiert wird. |
| MSP- \_ handle                   | \*m- \_ HT-Rückruf      | Das Handle für den TAPI3's-Befehl. Wird zum Auslösen von Ereignis Ereignissen verwendet.                                                                                                                                                                                                                                                                                             |
| DWORD                         | Mio. \_ dwmediatype   | Die Bitmaske der Medientypen bei diesem-Befehl.                                                                                                                                                                                                                                                                                                          |
| Cmsparray <itstream \*> | m- \_ Streams       | Die Liste der Streamobjekte im-Befehl.                                                                                                                                                                                                                                                                                                           |
| Cmspcritsection               | m- \_ Sperre          | Die Sperre, mit der die Datenstrom Listen geschützt werden.                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cmspcallbase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



