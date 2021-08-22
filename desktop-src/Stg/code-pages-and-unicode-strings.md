---
title: Codepages und Unicode-Zeichenfolgen
description: Ein weiterer Aspekt bei der Implementierung von IPropertySetStorage ist die Speicherung von Unicode-Eigenschaftsnamen in der Eigenschafts-ID 0 (dem Eigenschaftennamenwörterbuch), die keine Unicode-Zeichenfolgen verwendet.
ms.assetid: 830c90c9-d2a5-4ecf-8cb6-9950ed5320bf
keywords:
- Codepages und Unicode-Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a1d5a830d3d4e2fccbb61563e7a8a0447d74e7c427e5e2e0434e7194a2ad3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663600"
---
# <a name="code-pages-and-unicode-strings"></a>Codepages und Unicode-Zeichenfolgen

Ein weiterer Aspekt bei der Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ist die Speicherung von Unicode-Eigenschaftsnamen in der Eigenschafts-ID 0 (dem Eigenschaftennamenwörterbuch), die keine Unicode-Zeichenfolgen verwendet.

Unicode hat offiziell den Codepagewert 1200. Um Unicode-Werte im Eigenschaftennamenwörterbuch zu speichern, verwenden Sie den Codepagewert 1200 für den gesamten Eigenschaftensatz (in Eigenschafts-ID 1), der durch das Fehlen des **PROPSETFLAG \_ ANSI-Flags** in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)angegeben wird. Beachten Sie, dass dies den Nebeneffekt hat, dass alle Zeichenfolgenwerte in der in Unicode festgelegten Eigenschaft gespeichert werden. In allen Codepages ist die Anzahl, die am Anfang eines **VT \_ LPSTR** gefunden wurde, eine Byteanzahl, keine Zeichenanzahl. Dies ist erforderlich, um Kompatibilität mit Clients früherer Versionen zu gewährleisten.

Die Verbunddateiimplementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) erstellt alle neuen Eigenschaftensätze vollständig entweder in Unicode (Codepage 1200) oder auf der aktuellen SYSTEM-ANSI-Codepage. Dies wird durch das Fehlen oder Vorhandensein des **PROPSETFLAG \_ ANSI-Flags** im *grfFlags-Parameter* von [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)gesteuert.

Erstellen und öffnen Sie Eigenschaftensätze als Unicode. Um dies zu implementieren, legen Sie das **PROPSETFLAG \_ ANSI-Flag** nicht im *grfFlags-Parameter* von [**IPropertySetStorage::Create fest.**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) Vermeiden Sie die Verwendung von **VT \_ LPSTR-Werten,** und verwenden Sie stattdessen **VT \_ LPWSTR-Werte.** Wenn die Codepage des Eigenschaftensatzes Unicode ist, werden **VT \_ LPSTR-Zeichenfolgenwerte** bei der Speicherung in Unicode und beim Abrufen wieder in Multibyte-Zeichenfolgenwerte konvertiert.

Das Festlegen des **PROPSETFLAG-ANSI-Flags, \_** das durch einen Aufruf von [**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat) gemeldet wird, gibt an, ob die zugrunde liegende Codepage Unicode ist oder nicht. Beachten Sie, dass Eigenschafts-ID 1 explizit gelesen werden kann, um die Codepage zu erlernen.

Sie können über einen Aufruf von [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)auf Die Eigenschafts-ID 1 zugreifen. Sie ist jedoch schreibgeschützt und kann nicht mit [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)aktualisiert werden. Darüber hinaus kann es nicht mit [**DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)gelöscht werden.

 

 




