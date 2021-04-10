---
title: Dodownloadproperty-Enumeration
description: Gibt die ID der Eigenschaften für den Downloadvorgang an.
keywords:
- Dodownloadproperty-Enumeration, dodownloadproperty
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
ms.openlocfilehash: bb8ec6ad8cc55239522f953c6a81a8bf7b2b62ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105333"
---
# <a name="dodownloadproperty-enumeration"></a>Dodownloadproperty-Enumeration

Die **dodownloadproperty** -Enumeration gibt die ID der Eigenschaften für den Downloadvorgang an. Diese Enumeration wird von der **idodownload** -Schnittstelle verwendet und durch einen Variant-Wert ausgeführt, bei dem der Werttyp enthalten ist.

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
| DODownloadProperty_Id | Schreibgeschützt. Verwenden Sie diese Eigenschaft, um die ID zu erhalten, die den Download eindeutig identifiziert. Der Varianttyp ist VT_BSTR. |
| DODownloadProperty_Uri | Verwenden Sie diese Eigenschaft, um den Remote-URI-Pfad der herunter zuladenden Ressource festzulegen oder zu erhalten. Diese Eigenschaft ist nur erforderlich, wenn *DODownloadProperty_ContentId* nicht angegeben wird. Der Varianttyp ist VT_BSTR. |
| DODownloadProperty_ContentId | Verwenden Sie diese Eigenschaft, um die eindeutige Download-Inhalts-ID festzulegen oder zu erhalten. Diese Eigenschaft ist nur erforderlich, wenn *DODownloadProperty_Uri* nicht angegeben wird. Der Varianttyp ist VT_BSTR. |
| DODownloadProperty_DisplayName | Dies ist optional. Verwenden Sie diese Eigenschaft, um den Namen der Download Anzeige festzulegen oder zu erhalten. Der Varianttyp ist VT_BSTR. |
| DODownloadProperty_LocalPath | Verwenden Sie diese Eigenschaft, um den Namen des lokalen Pfads zum Speichern der Downloaddatei festzulegen oder zu erhalten. Wenn der Pfad nicht vorhanden ist, wird versucht, ihn unter den Berechtigungen des Aufrufers zu erstellen. Diese Eigenschaft ist nur erforderlich, wenn keine *DODownloadProperty_StreamInterface* bereitgestellt wurde. Der Varianttyp ist VT_BSTR. |
| DODownloadProperty_HttpCustomHeaders | Dies ist optional. Verwenden Sie diese Eigenschaft, um benutzerdefinierte HTTP-Anforderungs Header festzulegen oder zu erhalten. Diese Header werden bei http-Datei Anforderungs Vorgängen berücksichtigt. Die Header müssen bereits als Standard-HTTP-Header formatiert sein. Der Varianttyp ist VT_BSTR. |
| DODownloadProperty_CostPolicy | Dies ist optional. Verwenden Sie diese Eigenschaft, um einen der **dodownloadcostpolicy** -Enumerationswerte festzulegen oder zu erhalten. Der Varianttyp ist VT_UI4. |
| DODownloadProperty_SecurityFlags | Optionaler Schreibzugriff. Verwenden Sie diese Eigenschaft, um die standardmäßigen WinHTTP-sicherheitsflags (**WINHTTP_OPTION_SECURITY_FLAGS**) festzulegen oder zu erhalten. Der Varianttyp ist VT_UI4.</br></br>Die folgenden Flags werden unterstützt:</br>SECURITY_FLAG_IGNORE_CERT_CN_INVALID. Ermöglicht einen ungültigen allgemeinen Namen in einem Zertifikat.</br>SECURITY_FLAG_IGNORE_CERT_DATE_INVALID. Ermöglicht ein ungültiges Zertifikat Datum.</br>SECURITY_FLAG_IGNORE_UNKNOWN_CA. Lässt eine ungültige Zertifizierungsstelle zu.</br>SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE. Ermöglicht die Einrichtung der Identität eines Servers mit einem nicht-Serverzertifikat.</br>WINHTTP_ENABLE_SSL_REVOCATION. Ermöglicht SSL-Sperrung. Wenn dieses Flag festgelegt ist, werden die obigen Flags ignoriert. |
| DODownloadProperty_CallbackFreqPercent | Dies ist optional. Verwenden Sie diese Eigenschaft, um die Rückruf Häufigkeit basierend auf dem Download Prozentsatz festzulegen. Der Varianttyp ist VT_UI4. |
| DODownloadProperty_CallbackFreqSeconds | Dies ist optional. Verwenden Sie diese Eigenschaft, um die Rückruf Häufigkeit basierend auf der Downloadzeit festzulegen oder zu erhalten. Der Standardwert ist jede Sekunde. Der Varianttyp ist VT_UI4. |
| DODownloadProperty_NoProgressTimeoutSeconds | Dies ist optional. Verwenden Sie diese Eigenschaft, um die Download Timeout Länge für keinen Fortschritt festzulegen oder zu erhalten. Der minimal zulässige Wert ist 60 Sekunden ohne Download Aktivität. Der Varianttyp ist VT_UI4. |
| DODownloadProperty_ForegroundPriority | Dies ist optional. Verwenden Sie diese Eigenschaft, um die aktuelle Download Priorität festzulegen oder zu erhalten. VARIANT_TRUE Wert wird der Download mit höherer Priorität in den Vordergrund gebracht. Der Standardwert ist die Hintergrund Priorität. Der Varianttyp ist VT_BOOL. |
| DODownloadProperty_BlockingMode | Dies ist optional. Verwenden Sie diese Eigenschaft, um den aktuellen Download Blockierungs Modus festzulegen oder zu erhalten. VARIANT_TRUE Wert bewirkt, dass **idodownload:: Start** blockiert wird, bis der Download beendet oder ein Fehler aufgetreten ist. Der Standardwert ist der Modus für die nicht Blockierung. Der Varianttyp ist VT_BOOL. |
| DODownloadProperty_CallbackInterface | Dies ist optional. Verwenden Sie diese Eigenschaft, um den Zeiger auf die **idodownloadstatus Callback** -Schnittstelle festzulegen, die für Download Rückrufe verwendet wird. Der Varianttyp ist VT_UNKNOWN. |
| DODownloadProperty_StreamInterface | Dies ist optional. Verwenden Sie diese Eigenschaft, um den Zeiger auf die IStream-Schnittstelle festzulegen, die für den streamdownloadtyp verwendet wird. Der Varianttyp ist VT_UNKNOWN. |
| DODownloadProperty_SecurityContext | Optionaler Schreibzugriff. Verwenden Sie diese Eigenschaft, um den Zertifikat Kontext festzulegen, der bei HTTP-Anforderungs Vorgängen verwendet werden soll. Der Wert muss aus serialisierten Bytes CERT_CONTEXT bestehen. Der Varianttyp ist (VT_ARRAY \| VT_UI1). |
| DODownloadProperty_NetworkToken | Optionaler Schreibzugriff. Verwenden Sie diese Eigenschaft, um das Netzwerk Token festzulegen, das bei http-Vorgängen verwendet werden soll. VARIANT_TRUE Wert bewirkt, dass das Identitäts Token des Aufrufers erfasst und VARIANT_FALSE das vorhandene Token löscht. Der Standardwert ist das Token des angemeldeten Benutzers. Der Varianttyp ist VT_BOOL. |
| DODownloadProperty_CorrelationVector | Dies ist optional. Legt einen spezifischen Korrelations Vektor für Telemetriezwecke fest. Der Varianttyp ist VT_BSTR. |
| DODownloadProperty_DecryptionInfo | Optionaler Schreibzugriff. Legt Entschlüsselungs Informationen in Form einer JSON-Zeichenfolge fest. Der Varianttyp ist VT_BSTR. |
| DODownloadProperty_IntegrityCheckInfo | Optionaler Schreibzugriff. Legt den Speicherort der Teil Hash Datei (PHF) fest, der von Do verwendet wird, um Lauf Zeit Integritätsprüfungen für den heruntergeladenen Inhalt auszuführen. Der Varianttyp ist VT_BSTR. |
| DODownloadProperty_IntegrityCheckMandatory | Dies ist optional. Legt ein boolesches Flag fest, das angibt, ob die Verwendung der Teil Hash Datei (PHF) obligatorisch ist. Wenn VARIANT_TRUE, wird der Download abgebrochen, wenn die Integritätsprüfung fehlschlägt. Der Varianttyp ist VT_BOOL. |
| DODownloadProperty_TotalSizeBytes | Dies ist optional. Gibt die Gesamtgröße des Downloads in Bytes an. Der Varianttyp ist VT_UI8. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Deliveryoptimizationdownloadtypes. h |
