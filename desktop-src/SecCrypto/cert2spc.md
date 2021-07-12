---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581978"
---
# <a name="cert2spc"></a>Cert2SPC

Das Cert2SPC-Tool erstellt mithilfe vorhandener [*X.509-Zertifikate*](../secgloss/x-gly.md) [](../secgloss/c-gly.md)ein [*Test-SPC (Software Publisher Certificate).*](../secgloss/s-gly.md) Cert2SPC kann mehrere X.509-Zertifikate in ein [*PKCS \# 7-Datenobjekt*](../secgloss/p-gly.md) mit Vorzeichen umschließen. Das Tool wird im \\ Ordner Bin des Installationspfads des Microsoft Windows Software Development Kit (SDK) installiert.

Cert2SPC ist als Teil des Windows SDK verfügbar, das Sie unter herunterladen <https://go.microsoft.com/fwlink/p/?linkid=84091> können.

> [!Note]
> Dieses Tool dient nur zu Testzwecken. Ein gültiges SPC wird von einer [*Zertifizierungsstelle*](../secgloss/c-gly.md)abgerufen.


**Cert2SPC** *Cert1.cer Cert2.cer* ... *Output.spc*

 



| Parameter              | BESCHREIBUNG                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1.cer Cert2.cer* ... | Namen der X.509-Zertifikate, die in das SPC aufgenommen werden sollen. Jeder Zertifikatname endet mit der ERWEITERUNG CER.                         |
| *Output.spc*            | Name des PKCS \# 7-Objekts, das die zu erstellenden X.509-Zertifikate enthält. Der Name der Ausgabedatei endet mit der Erweiterung .spc. |



 

 

 
