---
description: Die Zertifikat Dienste unterstützen die Erneuerung einer Zertifizierungsstelle (Certification Authority, ca).
ms.assetid: b6c76642-9a23-471e-af08-58e91d778f09
title: Erneuerung der Zertifizierungsstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de57cd16ae6fc4c90bfeea411a06efcb14d028b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959210"
---
# <a name="certification-authority-renewal"></a>Erneuerung der Zertifizierungsstelle

Die [*Zertifikat Dienste*](../secgloss/c-gly.md) unterstützen die Erneuerung einer Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca). Die Erneuerung ist das Ausstellen eines neuen Zertifikats für die Zertifizierungsstelle, um die Lebensdauer der Zertifizierungsstelle über das Enddatum des ursprünglichen Zertifikats hinaus zu verlängern. Sie können eine Zertifizierungsstelle als Aufgabe innerhalb des MMC-Snap-Ins "Zertifizierungsstelle" oder mithilfe des Certutil.exe Tools (mit dem Befehl " **-erneuercert** ") erneuern.

Jede Erneuerung führt zu einem neuen Zertifizierungsstellen Zertifikat. der Administrator kann jedoch entweder ein neues öffentliches/privates Schlüsselpaar generieren oder das vorhandene öffentliche/private Schlüsselpaar für das Zertifizierungsstellen Zertifikat wieder verwenden. Aus Gründen der Konsistenz und Integrität werden Zertifizierungsstellen Zertifikate und [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRL), die von der Zertifizierungsstelle vor der Verlängerung ausgestellt wurden, verfügbar sein, nachdem die Zertifizierungsstelle erneuert wurde. Um diese Informationen verfügbar zu machen, verwaltet der Zertifikat Dienst einen Index von Zertifizierungsstellen Zertifikaten, CRLs und Schlüsseln.

Die Indizes und Suffixnamen von Zertifizierungsstellen Zertifikaten und CRLs sind bei verschiedenen ca-Erneuerungs Vorgängen wie folgt.



| Vorgang                | ZS-Zertifikat Index | Suffix der Zertifizierungsstellen-Zertifikat Datei | CRL und Schlüssel Index | CRL und Key Container Name Suffix |
|--------------------------|----------------------|---------------------------------|-------------------|-----------------------------------|
| Ursprüngliche Installation der Zertifizierungsstelle | 0                    | ""                              | 0                 | ""                                |
| Erneuerung mit neuem Schlüssel     | 1                    | "(1)"                           | 1                 | "(1)"                             |
| Erneuter erneuter Schlüssel      | 2                    | "(2)"                           | 1                 | "(1)"                             |
| Erneuter erneuter Schlüssel      | 3                    | "(3)"                           | 1                 | "(1)"                             |
| Erneuerung mit neuem Schlüssel     | 4                    | "(4)"                           | 4                 | "(4)"                             |
| Erneuter erneuter Schlüssel      | 5                    | "(5)"                           | 4                 | "(4)"                             |
| Erneuerung mit neuem Schlüssel     | 6                    | "(6)"                           | 6                 | "(6)"                             |
| Erneuter erneuter Schlüssel      | 7                    | "(7)"                           | 6                 | "(6)"                             |



 

Bei der Installation einer Zertifizierungsstelle ist der Zertifikat Index NULL, und das Zertifikat Suffix ist "" (eine leere Zeichenfolge). Jedes Mal, wenn das Zertifikat erneuert wird (unabhängig davon, ob Schlüssel wieder verwendet werden), wird der Zertifikat Index um 1 erhöht, und das Name-Suffix der Zertifikat Datei wird zu einer Zeichenfolge in der Form "(*n*)", wobei " *n* " angibt, wie oft das Zertifizierungsstellen Zertifikat erneuert wurde. Nach der ersten Erneuerung lautet der Zertifikat Index 1, und das Suffix für die Zertifikat Datei lautet "(1)". Nach der zweiten Erneuerung lautet der Zertifikat Index 2, und das Suffix für die Zertifikat Datei lautet "(2)" usw.

Obwohl der Zertifizierungsstellen-Zertifikat Index und das Suffix jedes Mal um eins erhöht werden, wenn die Zertifizierungsstelle erneuert wird, werden die CRL-und Schlüssel Indizes und die Dateinamen Suffixe nur dann auf den ZS-Zertifikats Index festgelegt, wenn der Erneuerungs Vorgang ein neues öffentliches/privates Schlüsselpaar enthält. Wenn dies nicht der Fall ist, bleiben die Werte dieser Indizes und Suffixe identisch mit denen für den letzten Index. Während der Verlängerung gibt ein Administrator an, ob ein neues Schlüsselpaar generiert oder das vorhandene Schlüsselpaar verwendet wird. (Im MMC-Snap-in "Zertifizierungsstelle" gibt eine Option auf der Benutzeroberfläche ein neues oder ein vorhandenes Schlüsselpaar an. im Certutil.exe Tool erneuert der Befehl " **certutil-erneucert** " die Zertifizierungsstelle mit einem neuen Schlüsselpaar, während der Befehl " **certutil-erneuercert reusekeys** " die Zertifizierungsstelle mit dem vorhandenen Schlüsselpaar erneuert.)

Der CRL-Index ist direkt an den Schlüssel indexgebunden, der nur dann auf den ZS-Zertifikats Index festgelegt wird, wenn ein neues Schlüsselpaar für die Erneuerung verwendet wird. Nach der ersten Erneuerung (die ein neues Schlüsselpaar verwendet hat) wird der Index der CRL und des Schlüssels auf 1 festgelegt, und das Suffix der CRL und des Schlüssel Container namens lautet "(1)". Nach der zweiten Erneuerung bleibt der Index der CRL und des Schlüssels 1, und die CRL und das Schlüssel Container-Namen Suffix bleiben ebenfalls "(1)". Dies liegt daran, dass bei der zweiten Erneuerung das vorhandene Schlüsselpaar verwendet wurde und für jedes ZS-Schlüsselpaar nur eine CRL ausgegeben wird.

Sie können die indizierten Zertifizierungsstellen Zertifikate und CRLs abrufen, indem Sie die **getcertificateproperty** -Methode aufrufen (in den Schnittstellen [**icertserverexit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) und [**icertserverpolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) ). Wenn Sie bestimmte Eigenschaften abrufen, die sich auf das Zertifizierungsstellen Zertifikat oder die CRL beziehen, können Sie den NULL basierten Index des Zertifizierungsstellen Zertifikats an die Eigenschaftsnamen anfügen. Wenn Sie z. b. den CRL-Index abrufen möchten, der dem dritten Zertifikat der Zertifizierungsstelle entspricht, übergeben Sie die Eigenschaft "crlindex. 2" an [**icertserverpolicy:: getcertificateproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty); für die-Tabelle ist der abgerufene "crlindex. 2"-Eigenschafts Wert "1". Eine Eigenschaft mit dem Namen "certcount" kann verwendet werden, um zu bestimmen, wie oft die Zertifizierungsstelle ein Zertifizierungsstellen Zertifikat ausgestellt hat.

Zertifizierungsstellen Zertifikate und CRLs enthalten eine Erweiterung, die Informationen über das Zertifikat und den Schlüssel Index bereitstellt. Die Erweiterung ist in Wincrypt. h als szoid \_ certrv- \_ ca- \_ Version mit dem Wert "1.3.6.1.4.1.311.21.1" definiert. Die Erweiterungs Daten sind ein **DWORD** -Wert (als X509- \_ Ganzzahl in der Erweiterung codiert); die unteren 16 Bits sind der Zertifikat Index, und die hohen 16 Bits sind der Schlüssel Index.

Bei der Erstinstallation einer Zertifizierungsstelle wird der Zertifikat Index NULL und der Schlüssel Index NULL erzeugt. Die Erneuerung eines ZS-Zertifikats bewirkt, dass der Zertifikat Index inkrementiert wird. Wenn der Schlüssel in der Erneuerung wieder verwendet wird, ist der Schlüssel Index mit dem vorherigen Schlüssel Index identisch. Wenn der Schlüssel nicht wieder verwendet wird, entspricht der Schlüssel Index dem neuen Zertifikat Index.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Icertserverpolicy:: getcertificateproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**Icertserverexit:: getcertificateproperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> </dl>

 

 
