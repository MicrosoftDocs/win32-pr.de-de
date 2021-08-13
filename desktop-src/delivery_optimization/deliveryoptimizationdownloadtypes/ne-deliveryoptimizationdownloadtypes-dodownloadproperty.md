---
title: DODownloadProperty-Enumeration
description: Gibt die ID der Eigenschaften für den DO-Downloadvorgang an.
keywords:
- DODownloadProperty-Enumeration, DODownloadProperty
topic_type:
- apiref
api_name:
- DODownloadProperty
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 2e36dc783a7b2c7da23f4513f198b7871f97fe6576f60ffdd6f0fcbd7a11e3f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544575"
---
# <a name="dodownloadproperty-enumeration"></a>DODownloadProperty-Enumeration

Die **DODownloadProperty-Enumeration** gibt die ID der Eigenschaften für den DO-Downloadvorgang an. Diese Enumeration wird von der **IDODownload-Schnittstelle** verwendet und durch einen VARIANT-Wert ausgeführt, in dem der Typ des Werts enthalten ist.

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadProperty
{
  DODownloadProperty_Id = 0,
  DODownloadProperty_Uri,
  DODownloadProperty_ContentId,
  DODownloadProperty_DisplayName,
  DODownloadProperty_LocalPath,
  DODownloadProperty_HttpCustomHeaders,
  DODownloadProperty_CostPolicy,
  DODownloadProperty_SecurityFlags,
  DODownloadProperty_CallbackFreqPercent,
  DODownloadProperty_CallbackFreqSeconds,
  DODownloadProperty_NoProgressTimeoutSeconds,
  DODownloadProperty_ForegroundPriority,
  DODownloadProperty_BlockingMode,
  DODownloadProperty_CallbackInterface,
  DODownloadProperty_StreamInterface,
  DODownloadProperty_SecurityContext,
  DODownloadProperty_NetworkToken
  DODownloadProperty_CorrelationVector,
  DODownloadProperty_DecryptionInfo,
  DODownloadProperty_IntegrityCheckInfo,
  DODownloadProperty_IntegrityCheckMandatory,
  DODownloadProperty_TotalSizeBytes
} DODownloadProperty;
```

## <a name="constants"></a>Konstanten

| Anforderung | Wert |
|-|-|
| DODownloadProperty_Id | Schreibgeschützt. Verwenden Sie diese Eigenschaft, um die ID zu erhalten, die den Download eindeutig identifiziert. Der VARIANT-Typ VT_BSTR. |
| DODownloadProperty_Uri | Verwenden Sie diese Eigenschaft, um den Remote-URI-Pfad der herunterzuladenden Ressource zu festlegen oder zu erhalten. Diese Eigenschaft ist nur erforderlich, *DODownloadProperty_ContentId* nicht bereitgestellt wird. Der VARIANT-Typ VT_BSTR. |
| DODownloadProperty_ContentId | Verwenden Sie diese Eigenschaft, um die eindeutige Inhalts-ID für den Download zu festlegen oder zu erhalten. Diese Eigenschaft ist nur erforderlich, *DODownloadProperty_Uri* nicht bereitgestellt wird. Der VARIANT-Typ VT_BSTR. |
| DODownloadProperty_DisplayName | Optional. Verwenden Sie diese Eigenschaft, um den Anzeigenamen für den Download zu festlegen oder zu erhalten. Der VARIANT-Typ VT_BSTR. |
| DODownloadProperty_LocalPath | Verwenden Sie diese Eigenschaft, um den Namen des lokalen Pfads zum Speichern der Downloaddatei zu festlegen oder zu erhalten. Wenn der Pfad nicht vorhanden ist, versucht DO, ihn unter den Berechtigungen des Aufrufers zu erstellen. Diese Eigenschaft ist nur erforderlich, *wenn DODownloadProperty_StreamInterface* nicht bereitgestellt wurde. Der VARIANT-Typ VT_BSTR. |
| DODownloadProperty_HttpCustomHeaders | Optional. Verwenden Sie diese Eigenschaft, um benutzerdefinierte HTTP-Anforderungsheader zu festlegen oder zu erhalten. DO enthält diese Header während HTTP-Dateianforderungsvorgängen. Die Header müssen bereits als HTTP-Standardheader formatiert sein. Der VARIANT-Typ VT_BSTR. |
| DODownloadProperty_CostPolicy | Optional. Verwenden Sie diese Eigenschaft, um einen der **DODownloadCostPolicy-Enumerationswerte** zu festlegen oder zu erhalten. Der VARIANT-Typ VT_UI4. |
| DODownloadProperty_SecurityFlags | Optionaler Schreibzugriff. Verwenden Sie diese Eigenschaft, um die WinHTTP-Standardsicherheitsflags ( WINHTTP_OPTION_SECURITY_FLAGS **) zu WINHTTP_OPTION_SECURITY_FLAGS.** Der VARIANT-Typ VT_UI4.</br></br>Die folgenden Flags werden unterstützt:</br>SECURITY_FLAG_IGNORE_CERT_CN_INVALID. Lässt einen ungültigen allgemeinen Namen in einem Zertifikat zu.</br>SECURITY_FLAG_IGNORE_CERT_DATE_INVALID. Lässt ein ungültiges Zertifikatdatum zu.</br>SECURITY_FLAG_IGNORE_UNKNOWN_CA. Lässt eine ungültige Zertifizierungsstelle zu.</br>SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE. Ermöglicht das Herstellen der Identität eines Servers mit einem Nicht-Serverzertifikat.</br>WINHTTP_ENABLE_SSL_REVOCATION. Lässt SSL-Sperrung zu. Wenn dieses Flag festgelegt ist, werden die oben genannten Flags ignoriert. |
| DODownloadProperty_CallbackFreqPercent | Optional. Verwenden Sie diese Eigenschaft, um die Rückrufhäufigkeit basierend auf dem Downloadprozentsatz zu festlegen oder zu erhalten. Der VARIANT-Typ VT_UI4. |
| DODownloadProperty_CallbackFreqSeconds | Optional. Verwenden Sie diese Eigenschaft, um die Rückrufhäufigkeit basierend auf der Downloadzeit zu festlegen oder zu erhalten. Der Standardwert ist alle eine Sekunde. Der VARIANT-Typ VT_UI4. |
| DODownloadProperty_NoProgressTimeoutSeconds | Optional. Verwenden Sie diese Eigenschaft, um die Download-Timeoutlänge für keinen Fortschritt fest- oder zu erhalten. Der akzeptierte Mindestwert beträgt 60 Sekunden ohne Downloadaktivität. Der VARIANT-Typ VT_UI4. |
| DODownloadProperty_ForegroundPriority | Optional. Verwenden Sie diese Eigenschaft, um die aktuelle Downloadpriorität zu festlegen oder zu erhalten. VARIANT_TRUE-Wert wird der Download mit höherer Priorität in den Vordergrund gestellt. Der Standardwert ist die Hintergrundpriorität. Der VARIANT-Typ VT_BOOL. |
| DODownloadProperty_BlockingMode | Optional. Verwenden Sie diese Eigenschaft, um den aktuellen Downloadblockierungsmodus zu festlegen oder zu erhalten. VARIANT_TRUE wert verursacht, **dass IDODownload::Start** blockiert wird, bis der Download abgeschlossen ist oder ein Fehler aufgetreten ist. Der Standardwert ist der Nichtblockierungsmodus. Der VARIANT-Typ VT_BOOL. |
| DODownloadProperty_CallbackInterface | Optional. Verwenden Sie diese Eigenschaft zum Festlegen oder Abrufen des Zeigers auf die **IDODownloadStatusCallback-Schnittstelle,** die für Downloadrückrufe verwendet wird. Der VARIANT-Typ VT_UNKNOWN. |
| DODownloadProperty_StreamInterface | Optional. Verwenden Sie diese Eigenschaft, um den Zeiger auf die IStream-Schnittstelle für den Streamdownloadtyp zu festlegen oder zu erhalten. Der VARIANT-Typ VT_UNKNOWN. |
| DODownloadProperty_SecurityContext | Optionaler Schreibzugriff. Verwenden Sie diese Eigenschaft, um den Zertifikatkontext für HTTP-Anforderungsvorgänge zu festlegen. Der Wert muss aus serialisierten Bytes von CERT_CONTEXT. Der VARIANT-Typ ist \| (VT_ARRAY VT_UI1). |
| DODownloadProperty_NetworkToken | Optionaler Schreibzugriff. Verwenden Sie diese Eigenschaft, um das Netzwerktoken für HTTP-Vorgänge festlegen. VARIANT_TRUE-Wert dazu, dass DO das Identitätstoken des Aufrufers erfasst, und VARIANT_FALSE vorhandene Token löschen. Der Standardwert ist das Token des angemeldeten Benutzers. Der VARIANT-Typ VT_BOOL. |
| DODownloadProperty_CorrelationVector | Optional. Legt einen bestimmten Korrelationsvektor für Telemetriezwecke fest. Der VARIANT-Typ VT_BSTR. |
| DODownloadProperty_DecryptionInfo | Optionaler Schreibzugriff. Legt Entschlüsselungsinformationen in Form einer JSON-Zeichenfolge fest. Der VARIANT-Typ VT_BSTR. |
| DODownloadProperty_IntegrityCheckInfo | Optionaler Schreibzugriff. Legt den Speicherort der Hashdatei (Piece Hash File, PHF) fest, der von DO verwendet wird, um Laufzeitintegritätsprüfungen für den heruntergeladenen Inhalt durchzuführen. Der VARIANT-Typ VT_BSTR. |
| DODownloadProperty_IntegrityCheckMandatory | Optional. Legt ein boolesches Flag fest, das angibt, ob die Verwendung der Stückhashdatei (PHF) obligatorisch ist. Wenn VARIANT_TRUE, wird der Download abgebrochen, wenn die Integritätsprüfung fehlschlägt. Der VARIANT-Typ VT_BOOL. |
| DODownloadProperty_TotalSizeBytes | Optional. Gibt die Gesamtgröße des Downloads in Bytes an. Der VARIANT-Typ VT_UI8. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, version 1809 Win32 applications only (Nur \[ Win32-Anwendungen der Version 1809)\] |
| **Header** | DeliveryOptimizationDownloadTypes.h |
