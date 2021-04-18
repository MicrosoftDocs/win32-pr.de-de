---
description: Die Peer Distribution-API definiert die folgenden Datentypen.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Datentypen der Peer Distribution-API (peerdist. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357762"
---
# <a name="peer-distribution-api-data-types"></a>Datentypen der Peer Distribution-API

Die Peer Distribution-API definiert die folgenden Datentypen.


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| Datentyp                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**Peer- \_ \_ Instanzhandle**          | Ein Handle, das der Peer Verteilungs Instanz zugeordnet ist. Dieses Handle wird von [**peerdiststartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)erstellt und in den meisten Peer Verteilungs Vorgängen verwendet.<br/>                                          |
| <span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**\_Inhalts Handle für Peer-dist \_**             | Ein Handle, das dem Inhalt zugeordnet ist. Dieses Handle wird von " [**Peer-distclientopencontent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) " erstellt und wird beim Öffnen, schließen, hinzufügen oder Veröffentlichen von Inhalten referenziert.<br/>                     |
| <span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**Peer- \_ ContentInfo- \_ handle** | Ein Handle, das Inhaltsinformationen zugeordnet ist. Dieses Handle wird von " [**eterdistserveropencontentinformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)" erstellt und beim Abrufen von codierten Inhaltsinformationen verwendet.<br/> |
| <span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**Peer- \_ Stream- \_ handle**                | Ein Handle, das einem Datenstrom zugeordnet ist. Dieses Handle wird von " [**eterdistserverpublishstream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) " erstellt, und es wird auf die Veröffentlichung, das Schließen oder das Hinzufügen von gestreuten Inhalten verwiesen.<br/>        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 Professional \[ Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>"Peer. h"</dt> </dl> |



 

 




