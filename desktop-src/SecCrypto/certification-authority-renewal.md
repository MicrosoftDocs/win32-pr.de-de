---
description: Zertifikatdienste unterstützen die Erneuerung einer Zertifizierungsstelle.
ms.assetid: b6c76642-9a23-471e-af08-58e91d778f09
title: Erneuerung der Zertifizierungsstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f486e877e2ce1645cddf0099599e120776194dfd71e4e8b131d936c85e1f45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993110"
---
# <a name="certification-authority-renewal"></a>Erneuerung der Zertifizierungsstelle

[*Zertifikatdienste*](../secgloss/c-gly.md) unterstützen die Erneuerung einer [*Zertifizierungsstelle.*](../secgloss/c-gly.md) Verlängerung ist die Ausstellung eines neuen Zertifikats für die Zertifizierungsstelle, um die Lebensdauer der Zertifizierungsstelle über das Enddatum des ursprünglichen Zertifikats hinaus zu verlängern. Sie können eine Zertifizierungsstelle als Aufgabe innerhalb des MMC-Snap-Ins der Zertifizierungsstelle oder mithilfe des Certutil.exe-Tools (mit dem **Befehl -renewCert)** erneuern.

Jede Verlängerung führt zu einem neuen Zertifizierungsstellenzertifikat. Der Administrator kann jedoch entweder ein neues Paar aus öffentlichem und privatem Schlüssel generieren oder das vorhandene Paar aus öffentlichem und privatem Schlüssel für das Zertifizierungsstellenzertifikat wiederverwenden. Aus Konsistenz- und Integritätserlangungs-, Zertifizierungsstellenzertifikaten und Zertifikatsperrlisten, [](../secgloss/c-gly.md) die von der Zertifizierungsstelle vor der Verlängerung ausgestellt wurden, sind nach der Erneuerung der Zertifizierungsstelle verfügbar. Um diese verfügbar zu machen, verwaltet Certificate Services einen Index von Zertifizierungsstellenzertifikaten, ZERTIFIKATSPERRLISTEN und Schlüsseln.

Die Indizes und Suffixnamen von Zertifizierungsstellenzertifikaten und Zertifikatsperrlisten während verschiedener Erneuerungsvorgänge der Zertifizierungsstelle lauten wie folgt.



| Vorgang                | Index des Zertifizierungsstellenzertifikats | Dateinamenssuffix des Zertifizierungsstellenzertifikats | Zertifikatsperrliste und Schlüsselindex | CRL- und Schlüsselcontainernamenssuffix |
|--------------------------|----------------------|---------------------------------|-------------------|-----------------------------------|
| Installation der ursprünglichen Zertifizierungsstelle | 0                    | ""                              | 0                 | ""                                |
| Erneuerung mit neuem Schlüssel     | 1                    | "(1)"                           | 1                 | "(1)"                             |
| Erneutes Wiederverwendnen des Schlüssels      | 2                    | "(2)"                           | 1                 | "(1)"                             |
| Erneutes Wiederverwendnen des Schlüssels      | 3                    | "(3)"                           | 1                 | "(1)"                             |
| Erneuerung mit neuem Schlüssel     | 4                    | "(4)"                           | 4                 | "(4)"                             |
| Erneutes Wiederverwendnen des Schlüssels      | 5                    | "(5)"                           | 4                 | "(4)"                             |
| Erneuerung mit neuem Schlüssel     | 6                    | "(6)"                           | 6                 | "(6)"                             |
| Erneutes Wiederverwendnen des Schlüssels      | 7                    | "(7)"                           | 6                 | "(6)"                             |



 

Wenn eine Zertifizierungsstelle installiert ist, ist der Zertifikatindex 0 (null), und das Zertifikatssuffix ist "" (eine leere Zeichenfolge). Jedes Mal, wenn das Zertifikat erneuert wird (unabhängig davon, ob Schlüssel wiederverwendet werden oder nicht), wird der Zertifikatindex um eins erhöht, und das Suffix des Zertifikatdateinamens wird zu einer Zeichenfolge der Form "(*n*)", wobei *n* die Anzahl der Erneuerungen des Zertifizierungsstellenzertifikats darstellt. Nach der ersten Verlängerung ist der Zertifikatindex 1, und das Suffix des Zertifikatdateinamens ist "(1)". Nach der zweiten Verlängerung ist der Zertifikatindex 2, und das Suffix des Zertifikatdateinamens ist "(2)" und so weiter.

Obwohl der Index und das Suffix des Zertifizierungsstellenzertifikats jedes Mal um eins erhöht werden, wenn die Zertifizierungsstelle erneuert wird, werden die Zertifikatsperrliste und die Schlüsselindizes und die Dateinamenssuffixe nur dann auf den Zertifizierungsstellenzertifikatindex festgelegt, wenn der Erneuerungsprozess ein neues Paar aus öffentlichem und privatem Schlüssel enthält. Wenn dies nicht der Wert ist, bleiben die Werte dieser Indizes und Suffixe unverändert wie für den letzten Index. Während der Verlängerung gibt ein Administrator an, ob ein neues Schlüsselpaar generiert oder das vorhandene Schlüsselpaar verwendet wird. (Im MMC-Snap-In der Zertifizierungsstelle gibt eine Option auf der Benutzeroberfläche ein neues oder vorhandenes Schlüsselpaar an. Im Certutil.exe-Tool erneuert der Befehl **certutil -renewCert** die Zertifizierungsstelle mit einem neuen Schlüsselpaar, während der Befehl **certutil -renewCert ReuseKeys** die Zertifizierungsstelle mit dem vorhandenen Schlüsselpaar erneuert.)

Der Zertifikatsperrlistenindex ist direkt an den Schlüsselindex gebunden, der nur dann auf den Zertifizierungsstellenzertifikatindex festgelegt wird, wenn ein neues Schlüsselpaar für die Erneuerung verwendet wird. Nach der ersten Verlängerung (bei der ein neues Schlüsselpaar verwendet wurde) wird der Index der Zertifikatsperrliste und des Schlüssels auf 1 festgelegt, und die Zertifikatsperrliste und das Suffix des Schlüsselcontainernamens sind "(1)". Nach der zweiten Verlängerung bleibt der Index der Zertifikatsperrliste und des Schlüssels jedoch 1, und die Zertifikatsperrliste und das Namenssuffix des Schlüsselcontainers bleiben ebenfalls "(1)"; Dies liegt daran, dass bei der zweiten Erneuerung das vorhandene Schlüsselpaar verwendet wurde und nur eine Zertifikatsperrliste für jedes Schlüsselpaar der Zertifizierungsstelle ausgestellt wird.

Sie können die indizierten Zertifizierungsstellenzertifikate und CRLs abrufen, indem Sie die **GetCertificateProperty-Methode** aufrufen (sowohl in den [**Schnittstellen ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) als auch [**ICertServerPolicy).**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) Wenn Sie bestimmte Eigenschaften im Zusammenhang mit dem Zertifizierungsstellenzertifikat oder der Zertifikatsperrliste abrufen, können Sie den nullbasierten Index des Zertifizierungsstellenzertifikats an die Eigenschaftennamen anfügen. Um beispielsweise den Zertifikatsperrlistenindex abzurufen, der dem dritten Zertifikat der Zertifizierungsstelle entspricht, übergeben Sie die Eigenschaft "CRLIndex.2" an [**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty); für die Tabelle wäre der abgerufene Eigenschaftswert "CRLIndex.2" 1. Mit einer Eigenschaft namens "CertCount" kann ermittelt werden, wie oft die Zertifizierungsstelle ein Zertifizierungsstellenzertifikat ausgestellt hat.

Zertifizierungsstellenzertifikate und Zertifikatsperrlisten enthalten eine Erweiterung, die Informationen zum Zertifikat und Schlüsselindex enthält. Die Erweiterung ist in Wincrypt.h als szOID CERTSRV CA VERSION mit dem Wert \_ \_ \_ "1.3.6.1.4.1.311.21.1" definiert. Die Erweiterungsdaten sind **ein DWORD-Wert** (in der Erweiterung als X.509 INTEGER codiert). Die unteren 16 Bits sind der Zertifikatindex und die hohen 16 Bits sind der \_ Schlüsselindex.

Die Erstinstallation einer Zertifizierungsstelle erzeugt einen Zertifikatindex von 0 (null) und einen Schlüsselindex 0 (null). Durch die Erneuerung eines Zertifizierungsstellenzertifikats wird der Zertifikatindex erhöht. Wenn der Schlüssel bei der Erneuerung wiederverwendet wird, ist der Schlüsselindex mit dem vorherigen Schlüsselindex identisch. Wenn der Schlüssel nicht wiederverwendet wird, wird der Schlüsselindex mit dem neuen Zertifikatindex übereinstimmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerExit::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> </dl>

 

 
