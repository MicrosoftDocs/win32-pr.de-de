---
description: Verwenden Sie MakeCert-Befehle, um Testzertifikate mithilfe von Optionen zu erstellen, Internet Explorer Version 4.0 oder höher verfügbar sind.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Verwenden von MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321eccfc26e3fc5bf13a541e1aab6a41b3f5d0930beed03f6033211bf63ac689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971550"
---
# <a name="using-makecert"></a>Verwenden von MakeCert

In den folgenden Beispielen werden [MakeCert-Befehle](makecert.md) verwendet, um Testzertifikate mithilfe von Optionen zu erstellen, Internet Explorer Version 4.0 oder höher verfügbar sind.

-   Stellen Sie ein Zertifikat aus, das vom Standardteststamm ausgestellt wird. Speichern Sie das Zertifikat in einer Datei.

    **MakeCert** *MyNew.cer*

-   Stellen Sie ein Zertifikat aus, das vom Standardteststamm ausgestellt wird. Speichern Sie sie in einem Zertifikatspeicher.

    **MakeCert -ss** *MyNewStore*

-   Stellen Sie ein Zertifikat aus, das vom Standardteststamm ausgestellt wird. Erstellen Sie einen Schlüsselcontainer, und speichern Sie das Zertifikat sowohl in einem Speicher als auch in einer Datei.

    **MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer*

-   Stellen Sie ein Zertifikat aus, das vom Standardteststamm ausgestellt wird. Erstellen Sie eine Datei mit einem privaten Schlüssel, und speichern Sie das Zertifikat sowohl in einem Speicher als auch in einer Datei.

    **MakeCert -sv** *MyKeyFile* **-ss** *MyNewStore* *MyNew.cer*

-   Stellen Sie ein Zertifikat aus, das vom Standardteststamm ausgestellt wird. Erstellen Sie einen Schlüsselcontainer, speichern Sie das Zertifikat sowohl in einem Speicher als auch in einer Datei, und machen Sie den privaten Schlüssel exportierbar.

    **MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer* **-pe**

-   Stellen Sie ein Zertifikat mithilfe des Standardteststamms sicher. Speichern Sie das Zertifikat in einem Speicher. Erstellen Sie dann ein weiteres Zertifikat, das vom neu erstellten Zertifikat ausgestellt wird. Speichern Sie das zweite Zertifikat in einem anderen Speicher.

    **MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* **MakeCert -is** *MyNewStore* **-ss** *AnotherStore*

-   Stellen Sie ein Zertifikat mithilfe des Standardteststamms sicher. Speichern Sie das Zertifikat im My-Speicher. Erstellen Sie dann mithilfe des neu erstellten Zertifikats ein weiteres Zertifikat. Wenn im MY-Speicher mehrere Zertifikate gespeichert sind, muss das Zertifikat anhand seines allgemeinen Namens identifiziert werden.

    **MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my MakeCert -is my -in "XXZZYY" -ss** *AnotherStore*

-   Stellen Sie ein Zertifikat mithilfe des Standardteststamms sicher. Speichern Sie das Zertifikat im MY-Speicher und in einer Datei. Erstellen Sie dann mithilfe des neu erstellten Zertifikats *MyNew ein weiteres* Zertifikat. Wenn sich mehr als ein Zertifikat im MY-Speicher befindet, identifizieren Sie das erste Zertifikat eindeutig mithilfe des Zertifikatdateinamens.

    **MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my** *MyNew.cer* **MakeCert -is my -ic** *MyNew.cer* **-ss** *AnotherStore*

 

 



