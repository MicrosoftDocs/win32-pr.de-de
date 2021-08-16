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

Die **DODownloadProperty-Enumeration** gibt die ID der Eigenschaften für den DO-Downloadvorgang an. Diese Enumeration wird von der **IDODownload-Schnittstelle** verwendet und von einem VARIANT-Wert ausgeführt, in dem der Werttyp enthalten ist.

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
| DODownloadProperty_Id | Schreibgeschützt. Verwenden Sie diese Eigenschaft, um die ID abzurufen, die den Download eindeutig identifiziert. Variant-Typ ist VT_BSTR. |
| DODownloadProperty_Uri | Verwenden Sie diese Eigenschaft, um den Remote-URI-Pfad der herunterzuladende Ressource festzulegen oder abzurufen. Diese Eigenschaft ist nur erforderlich, wenn *DODownloadProperty_ContentId* nicht bereitgestellt wird. Variant-Typ ist VT_BSTR. |
| DODownloadProperty_ContentId | Verwenden Sie diese Eigenschaft, um die eindeutige Inhalts-ID für den Download festzulegen oder abzurufen. Diese Eigenschaft ist nur erforderlich, wenn *DODownloadProperty_Uri* nicht bereitgestellt wird. Variant-Typ ist VT_BSTR. |
| DODownloadProperty_DisplayName | Optional. Verwenden Sie diese Eigenschaft, um den Anzeigenamen des Downloads festzulegen oder abzurufen. Variant-Typ ist VT_BSTR. |
| DODownloadProperty_LocalPath | Verwenden Sie diese Eigenschaft, um den Namen des lokalen Pfads festzulegen oder abzurufen, um die Downloaddatei zu speichern. Wenn der Pfad nicht vorhanden ist, versucht DO, ihn unter den Berechtigungen des Aufrufers zu erstellen. Diese Eigenschaft ist nur erforderlich, wenn *DODownloadProperty_StreamInterface* nicht bereitgestellt wurde. Variant-Typ ist VT_BSTR. |
| DODownloadProperty_HttpCustomHeaders | Optional. Verwenden Sie diese Eigenschaft, um benutzerdefinierte HTTP-Anforderungsheader festzulegen oder abzurufen. Do schließt diese Header während HTTP-Dateianforderungsvorgängen ein. Die Header müssen bereits als HTTP-Standardheader formatiert sein. Variant-Typ ist VT_BSTR. |
| DODownloadProperty_CostPolicy | Optional. Verwenden Sie diese Eigenschaft, um einen der **DODownloadCostPolicy-Enumerationswerte** festzulegen oder abzurufen. Der VARIANT-Typ ist VT_UI4. |
| DODownloadProperty_SecurityFlags | Optionaler Schreibzugriff. Verwenden Sie diese Eigenschaft, um die WinHTTP-Standardsicherheitsflags (**WINHTTP_OPTION_SECURITY_FLAGS**) festzulegen oder abzurufen. Der VARIANT-Typ ist VT_UI4.</br></br>Die folgenden Flags werden unterstützt:</br>SECURITY_FLAG_IGNORE_CERT_CN_INVALID. Lässt einen ungültigen allgemeinen Namen in einem Zertifikat zu.</br>SECURITY_FLAG_IGNORE_CERT_DATE_INVALID. Lässt ein ungültiges Zertifikatdatum zu.</br>SECURITY_FLAG_IGNORE_UNKNOWN_CA. Lässt eine ungültige Zertifizierungsstelle zu.</br>SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE. Ermöglicht die Einrichtung der Identität eines Servers mit einem Nicht-Serverzertifikat.</br>WINHTTP_ENABLE_SSL_REVOCATION. Ermöglicht SSL-Sperrung. Wenn dieses Flag festgelegt ist, werden die obigen Flags ignoriert. |
| DODownloadProperty_CallbackFreqPercent | Optional. Verwenden Sie diese Eigenschaft, um die Rückrufhäufigkeit basierend auf dem Downloadprozentsatz festzulegen oder abzurufen. Der VARIANT-Typ ist VT_UI4. |
| DODownloadProperty_CallbackFreqSeconds | Optional. Verwenden Sie diese Eigenschaft, um die Rückrufhäufigkeit basierend auf der Downloadzeit festzulegen oder abzurufen. Der Standardwert ist jede Sekunde. Der VARIANT-Typ ist VT_UI4. |
| DODownloadProperty_NoProgressTimeoutSeconds | Optional. Verwenden Sie diese Eigenschaft, um die Downloadtimeoutlänge ohne Fortschritt festzulegen oder abzurufen. Der akzeptierte Mindestwert beträgt 60 Sekunden ohne Downloadaktivität. Der VARIANT-Typ ist VT_UI4. |
| DODownloadProperty_ForegroundPriority | Optional. Verwenden Sie diese Eigenschaft, um die aktuelle Downloadpriorität festzulegen oder abzurufen. VARIANT_TRUE Wert wird der Download mit höherer Priorität in den Vordergrund lädt. Der Standardwert ist die Hintergrundpriorität. Der VARIANT-Typ ist VT_BOOL. |
| DODownloadProperty_BlockingMode | Optional. Verwenden Sie diese Eigenschaft, um den aktuellen Downloadblockierungsmodus festzulegen oder abzurufen. VARIANT_TRUE Wert bewirkt, dass **IDODownload::Start** blockiert wird, bis der Download abgeschlossen ist oder ein Fehler aufgetreten ist. Der Standardwert ist der Nichtblockierungsmodus. Der VARIANT-Typ ist VT_BOOL. |
| DODownloadProperty_CallbackInterface | Optional. Verwenden Sie diese Eigenschaft, um den Zeiger auf die **IDODownloadStatusCallback-Schnittstelle** festzulegen oder abzurufen, die für Downloadrückrufe verwendet wird. Der VARIANT-Typ ist VT_UNKNOWN. |
| DODownloadProperty_StreamInterface | Optional. Verwenden Sie diese Eigenschaft, um den Zeiger auf die IStream-Schnittstelle festzulegen oder abzurufen, die für den Streamdownloadtyp verwendet wird. Der VARIANT-Typ ist VT_UNKNOWN. |
| DODownloadProperty_SecurityContext | Optionaler Schreibzugriff. Verwenden Sie diese Eigenschaft, um den Zertifikatkontext festzulegen, der bei HTTP-Anforderungsvorgängen verwendet werden soll. Der Wert muss aus serialisierten Bytes von CERT_CONTEXT bestehen. Der VARIANT-Typ ist (VT_ARRAY \| VT_UI1). |
| DODownloadProperty_NetworkToken | Optionaler Schreibzugriff. Verwenden Sie diese Eigenschaft, um das Netzwerktoken festzulegen, das bei HTTP-Vorgängen verwendet werden soll. VARIANT_TRUE Wert bewirkt, dass DO das Identitätstoken des Aufrufers erfasst und VARIANT_FALSE das vorhandene Token löscht. Der Standardwert ist das Token des angemeldeten Benutzers. Der VARIANT-Typ VT_BOOL. |
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
