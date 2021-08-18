---
description: Registriert einen Computer in einer Zertifikathierarchie mithilfe einer Vorlage, eines Zertifikatanzeigenamens und der Zertifikatbeschreibung.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: enrollSimpleMachineCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb533dc2c0d262a64f8fd1d2245c310880586c04900ef028e7c2609f1a6b4577
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976900"
---
# <a name="enrollsimplemachinecert"></a>enrollSimpleMachineCert

Im Beispiel enrollSimpleMachineCert wird ein Computer in einer Zertifikathierarchie mithilfe einer Vorlage, eines Zertifikatanzeigenamens und der Zertifikatbeschreibung registriert.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird standardmäßig eine C++-Version des Beispiels im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ EnrollSimpleMachineCert installiert. Eine VBScript-Version wird im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VBS \\ EnrollSimpleMachineCert installiert.

## <a name="discussion"></a>Diskussion (Discussion)

Das Beispiel enrollSimpleMachineCert:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile sollte den Namen der Vorlage, einen Zertifikatanzeigenamen und eine Zertifikatbeschreibung enthalten.
2.  Erstellt ein [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) und initialisiert es mithilfe der in der Befehlszeile angegebenen Vorlage. Der ContextAdministratorForceMachine-Wert für den ersten Parameter gibt an, dass das Zertifikat von einem Administrator angefordert wird, der im Auftrag eines Computers handelt.
3.  Fügt dem Registrierungsobjekt den Anzeigenamen und die Beschreibung hinzu.
4.  Versucht, die Zertifikatanforderung zu registrieren, und überprüft den Status des Prozesses. Die checkEnrollStatus-Funktion ist in enrollCommon.cpp definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 



