---
description: MTP-Erweiterungs Eigenschaften
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: MTP-Erweiterungs Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356237"
---
# <a name="mtp-extension-properties"></a>MTP-Erweiterungs Eigenschaften

Eigenschaften beschreiben Objekte, Eigenschaften, Ressourcen und Geräte.

## <a name="vendor-extended-object-properties"></a>Vom Hersteller erweiterte Objekteigenschaften

Wenn ein Gerätehersteller eine vom Hersteller erweiterte Eigenschaft für ein Geräte Objekt erstellt, werden die **\_ Eigenschaften des \_ MTP-Herstellers \_ für \_ Erweiterte \_ Objekte \_ des MTP** -Herstellers mit dem Eigenschafts Code des Objekts kombiniert, um eine **PropertyKey** -Struktur zu erstellen.

Wenn z. b. der Eigenschafts Code des Objekts 0xd801 ist, würde der resultierende **PropertyKey** wie im folgenden Beispiel gezeigt lauten:


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a>Vom Hersteller erweiterte Geräteeigenschaften

Wenn ein Gerätehersteller eine vom Hersteller erweiterte Eigenschaft für ein Gerät erstellt, kombiniert er die **Eigenschaften des \_ \_ MTP- \_ Herstellers \_ für \_ Erweiterte \_ Geräteeigenschaften des MTP** -Herstellers mit dem Eigenschafts Code des Objekts, um eine **PropertyKey** -Struktur zu erstellen.

Wenn z. b. der Eigenschafts Code des Objekts 0xd001 ist, würde der resultierende **PropertyKey** wie im folgenden Beispiel gezeigt lauten:


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützen von MTP-Erweiterungen](supporting-mtp-extensions.md)
</dt> </dl>

 

 



