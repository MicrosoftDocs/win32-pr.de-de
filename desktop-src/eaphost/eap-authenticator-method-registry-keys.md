---
title: Registrierungswerte der EAP Authenticator-Methode
description: Erfahren Sie mehr über EAP Authenticator-Methodenregistrierungswerte. Diese spezifischen Registrierungswerte sind für EAP-Authentifikatormethoden erforderlich.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1db88a910a40519533ffddae40c1e1cc04d36b62f3d3ad6543ddd4a2999373e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984310"
---
# <a name="eap-authenticator-method-registry-values"></a>Registrierungswerte der EAP Authenticator-Methode

Für EAP-Authentifikatormethoden sind bestimmte Registrierungswerte erforderlich.

## <a name="eap-authenticator-method-dll-paths"></a>EAP Authenticator-Methoden-DLL-Pfade

Der folgende Pfad gibt den Registrierungsspeicherort für reguläre EAP-Authentifikatormethoden-DLLs an.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ *&lt; AuthorId &gt;* \\ * &lt; EapTypeId&gt;***

Beispielsweise wird ein Installationsregistrierungspfad für die EAP-Authentifikatormethode mit der **AuthorId** "311" (der angibt, dass "Microsoft" der Autor ist) und der **EapTypeId** "40" wie folgt angezeigt.

**HKLM \\ System \\ CCS Services \\ \\ Eaphost \\ Methods \\ 311 \\ 40**

Der folgende Pfad gibt den Registrierungsspeicherort für erweiterte EAP-Authentifikatormethoden-DLLs an.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ * &lt; VendorType&gt;***

Ein Installationsregistrierungspfad für die EAP-Authentifikatormethode mit der **AuthorId** "311" (gibt an, dass "Microsoft" der Autor ist), eine **VendorId** von "311" und eine **EapTypeId** von "40" wird wie folgt angezeigt.

**HKLM \\ System \\ CCS Services \\ \\ Eaphost \\ Methods \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Weitere Informationen zur Zuordnung von EAP-Methodentypen finden Sie in Abschnitt 6.2 von [RFC 3748.](https://go.microsoft.com/fwlink/p/?linkid=84016)

 

## <a name="registry-values"></a>Registrierungswerte

Die folgenden Registrierungswerte für die Authentifikatormethode sind erforderlich.

-   [AuthenticatorDllPath](#authenticatordllpath)
-   [AuthenticatorFriendlyName](#authenticatorfriendlyname)

Neben den oben genannten Registrierungswerten wird der folgende Registrierungswert für die Authentifikatormethode empfohlen.

-   [Eigenschaften](#properties)

Die verbleibenden Authentifikatormethodenregistrierungswerte sind optional.

-   [ConfigCLSID](#configclsid)
-   [StandaloneSupported](#standalonesupported)

## <a name="authenticatordllpath"></a>AuthenticatorDllPath



| Konstanter Wert | AuthenticatorDllPath                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| type           | REG \_ EXPAND \_ SZ                                                                                               |
| BESCHREIBUNG    | Der Pfad zur DLL der EAP-Authentifikatormethode. Beispiel: %SystemRoot% \\ system32 \\ &lt; Name der DLL \_ \_ &gt;.dll. |



 

## <a name="authenticatorfriendlyname"></a>AuthenticatorFriendlyName



| Konstanter Wert | AuthenticatorFriendlyName                                                          |
|----------------|------------------------------------------------------------------------------------|
| type           | REG \_ SZ                                                                            |
| BESCHREIBUNG    | Zeichenfolge, die den Anzeigenamen für die EAP-Authentifikatormethode enthält. |



 

## <a name="configclsid"></a>ConfigCLSID



| Konstanter Wert | ConfigCLSID                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ SZ                                                                                                                               |
| BESCHREIBUNG    | Zeichenfolge, die die Konfigurationsklassen-GUID für diese Authentifikatormethode im Format {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} enthält |



 

## <a name="properties"></a>Eigenschaften



| Konstanter Wert | Eigenschaften                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ DWORD                                                                                                                                                  |
| BESCHREIBUNG    | Bits im DWORD werden so festgelegt, dass unterstützung für die -Eigenschaft angegeben wird. Eine Liste der unterstützten Werte finden Sie unter [**EAP-Methodeneigenschaften.**](eap-method-properties.md) |



 

## <a name="standalonesupported"></a>StandaloneSupported



| Konstanter Wert | StandaloneSupported                                             |
|----------------|-----------------------------------------------------------------|
| type           | REG \_ DWORD                                                      |
| BESCHREIBUNG    | 0, wenn es sich um eine eigenständige Authentifikatormethode handelt. 1, wenn nicht. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungsschlüssel für EAP-Peermethoden](eap-peer-method-registry-keys.md)
</dt> <dt>

[Registrierungskonfiguration für erweiterte EAP-Typen](registry-keys-for-eap-methods.md)
</dt> <dt>

[Verwenden von EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




