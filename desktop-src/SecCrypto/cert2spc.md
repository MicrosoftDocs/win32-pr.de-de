---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1680f8fe426c2e3a62cac0674928a1520b402357
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363903"
---
# <a name="cert2spc"></a>Cert2SPC

Das Cert2SPC-Tool erstellt ein Test [*Software Publisher-Zertifikat*](../secgloss/s-gly.md) (SPC) mithilfe vorhandener [*X. 509*](../secgloss/x-gly.md) - [*Zertifikate*](../secgloss/c-gly.md). Cert2SPC kann mehrere X. 509-Zertifikate in ein mit [*PKCS \# 7*](../secgloss/p-gly.md) signiertes signiertes Datenobjekt umschließen. Das Tool wird im \\ Ordner bin des Installations Pfads des Microsoft Windows Software Development Kit (SDK) installiert.

Cert2SPC ist als Teil des Windows SDK verfügbar, das Sie von herunterladen können <https://go.microsoft.com/fwlink/p/?linkid=84091> .

> [!Note]
> Dieses Tool ist nur für Testzwecke vorgesehen. Ein gültiges SPC wird von einer [*Zertifizierungs*](../secgloss/c-gly.md)Stelle abgerufen.


**Cert2SPC** *Cert1. CER Cert2. CER* ... *Ausgabe. SPC*

 



|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1. CER Cert2. CER* ... | Namen der X. 509-Zertifikate, die in das SPC eingeschlossen werden sollen. Jeder Zertifikat Name endet mit der Erweiterung ". cer".                         |
| *Ausgabe. SPC*            | Der Name des PKCS \# 7-Objekts, das die zu erstellenden X. 509-Zertifikate enthält. Der Name der Ausgabedatei endet mit der Erweiterung. SPC. |



 

 

 
