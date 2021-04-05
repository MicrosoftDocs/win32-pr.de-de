---
description: Verwenden Sie Makecert-Befehle zum Erstellen von Test Zertifikaten mithilfe der Optionen, die in Internet Explorer Version 4,0 oder höher verfügbar sind.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Verwenden von Makecert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068b10d5ce50141ff657379f9c5106cf2733d969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753448"
---
# <a name="using-makecert"></a>Verwenden von Makecert

In den folgenden Beispielen werden [Makecert](makecert.md) -Befehle zum Erstellen von Test Zertifikaten mithilfe der Optionen verwendet, die in Internet Explorer Version 4,0 oder höher verfügbar sind.

-   Erstellen Sie ein Zertifikat, das vom Standardtest Stamm ausgestellt wird. Speichern Sie das Zertifikat in einer Datei.

    **Makecert** *mynew. CER*

-   Erstellen Sie ein Zertifikat, das vom Standardtest Stamm ausgestellt wird. Speichern Sie Sie in einem Zertifikat Speicher.

    **Makecert-SS** *mynewstore*

-   Erstellen Sie ein Zertifikat, das vom Standardtest Stamm ausgestellt wird. Erstellen Sie einen Schlüssel Container, und speichern Sie das Zertifikat in einem Geschäft und in einer Datei.

    **Makecert-SK** *mynewkey* **-SS** *mynewstore* *mynew. CER*

-   Erstellen Sie ein Zertifikat, das vom Standardtest Stamm ausgestellt wird. Erstellen Sie eine Datei mit einem privaten Schlüssel, und speichern Sie das Zertifikat sowohl in einem Speicher als auch in einer Datei.

    **Makecert-SV** *mykeyfile* **-SS** *mynewstore* *mynew. CER*

-   Erstellen Sie ein Zertifikat, das vom Standardtest Stamm ausgestellt wird. Erstellen Sie einen Schlüssel Container, speichern Sie das Zertifikat in einem Geschäft und in einer Datei, und machen Sie den privaten Schlüssel exportierbar.

    **Makecert-SK** *mynewkey* **-SS** *mynewstore* *mynew. CER* **-PE**

-   Erstellen Sie ein Zertifikat mit dem Standardtest Stamm. Speichern Sie das Zertifikat in einem Speicher. Erstellen Sie dann ein anderes Zertifikat, das vom neu erstellten Zertifikat ausgestellt wird. Speichern Sie das zweite Zertifikat in einem anderen Speicher.

    **Makecert-SK** *mynewkey* **-SS** *mynewstore* **Makecert-ist** *mynewstore* **-SS** *anotherstore*

-   Erstellen Sie ein Zertifikat mit dem Standardtest Stamm. Speichern Sie das Zertifikat im eigenen Speicher. Erstellen Sie dann mithilfe des neu erstellten Zertifikats ein weiteres Zertifikat. Wenn im eigenen Speicher mehr als ein Zertifikat vorhanden ist, muss das Zertifikat mithilfe seines allgemeinen Namens identifiziert werden.

    **Makecert-SK** *mynewkey* **-n "CN = xxzzyy"-SS My Makecert-is my-in "xxzzyy"-SS** *anotherstore*

-   Erstellen Sie ein Zertifikat mit dem Standardtest Stamm. Speichern Sie das Zertifikat im eigenen Speicher und in einer Datei. Erstellen Sie dann mit dem neu erstellten *mynew* -Zertifikat ein anderes Zertifikat. Wenn im eigenen Speicher mehr als ein Zertifikat vorhanden ist, identifizieren Sie das erste Zertifikat mit dem Namen der Zertifikat Datei eindeutig.

    **Makecert-SK** *mynewkey* **-n "CN = xxzzyy"-SS My** *mynew. CER* **Makecert-ist My-IC** *mynew. CER* **-SS** *anotherstore*

 

 



