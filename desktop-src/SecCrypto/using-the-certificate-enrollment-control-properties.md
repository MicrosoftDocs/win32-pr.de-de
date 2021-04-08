---
description: Jede Zertifikat Registrierungs Steuerungs Eigenschaft ist Lese-/Schreibzugriff und verfügt über einen initialisierten Standardwert sowie einen Satz zulässiger Werte.
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: Verwenden der Eigenschaften der Zertifikat Registrierungs Steuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753433"
---
# <a name="using-the-certificate-enrollment-control-properties"></a>Verwenden der Eigenschaften der Zertifikat Registrierungs Steuerung

Jede Zertifikat Registrierungs Steuerungs Eigenschaft ist Lese-/Schreibzugriff und verfügt über einen initialisierten Standardwert sowie einen Satz zulässiger Werte. Sie können eine Eigenschaft auf einen beliebigen Wert in dieser Gruppe festlegen, um das Verhalten von Methoden zu ändern, die die-Eigenschaft verwenden. Um ein gewünschtes Verhalten zu erzielen, legen Sie die-Eigenschaft fest, bevor Sie die-Methode mit dem Wert dieser Eigenschaft aufzurufen.

Beachten Sie jedoch, dass nach dem Aufrufen der folgenden Methoden

-   [**acceptPKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [**acceptFilePKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [**createPKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [**createFilePKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

die zurück setzung der folgenden Eigenschaften ist blockiert.

-   [**ProviderType**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [**KeySpec**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [**Providerflags**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [**Container Name**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [**ProviderName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

es sei denn, die [**ICEnroll4:: Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) -Methode wird aufgerufen.

Informationen zu einzelnen Eigenschaften und Methoden finden Sie in den Referenz Themen zu den Eigenschaften und Methoden in der [kryptografiereferenz](cryptography-reference.md).

Die folgenden Abschnitte enthalten sprachspezifische Informationen zum Festlegen und Abrufen der Eigenschaften der Zertifikat Registrierungs Steuerung:

-   [Eigenschaften der Zertifikat Registrierungs Steuerung in C++](certificate-enrollment-control-properties-in-c-.md)

 

 
